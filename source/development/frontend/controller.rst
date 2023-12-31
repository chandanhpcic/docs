===========================
Using controllers and views
===========================

-------
General
-------

After routing is performed, the controller takes care of the actual code
to execute for the request. Because we want to implement some basics for
every request that gets processed you should inherit from our base
classes to ensure basic functionality such as authorisation and CSRF
protection.

Controllers are placed in the directory /usr/local/reticen8/mvc/app/controllers/<Vendor\_name>/<Module\_name>/
and should use the standard Phalcon naming conventions, suffix Controller.php on
every class file and suffix Action on all action methods.

For a detailed description of how Controllers work in Phalcon, please
look at the Phalcon documentation at http://docs.phalconphp.com/en/latest/reference/controllers.html

----------------------
View based controllers
----------------------

For rendering standard pages we have chosen to use Volt templates, the
base controller to inherit from in this case is
Reticen8\\Base\\ControllerBase and should take care of binding a
template to the controller. Every template automatically receives
standard features (such as the menu system).

The wireframe for implementing a single action should look like this:

.. code-block:: php

    <?php
        public function indexAction()
        {
           // address some variables to pass through the view
            $this->view->my_variable1 = 'test 1';
            $this->view->my_variable2 = 'test 2';
           // pick a template
            $this->view->pick('SampleVendor/Sample/index');
        }

And the volt template SampleVendor/Sample/index.volt could contain something like:

.. code-block:: html

      the contents of my_variable1 => <b> {{ my_variable1 }} </b> <br>
      the contents of my_variable2 => <b> {{ my_variable2 }} </b> <br>

A full example can be found in the Reticen8\\Sample controller
directory.

More information on how to write Volt pages can be found here :
http://docs.phalconphp.com/en/latest/reference/volt.html

---------------------
User forms
---------------------

When designers need forms for users to input data, they can use the :code:`getForm()` method on our standard controller
to feed a simple xml file as definition for the template engine to use. The example section contains a step by step
guide how to use these.

The getForm() method itself merily passes the structure to thew view, which can use this information to render
forms on page load (statically).
In our standard layout `partials <https://github.com/reticen8/core/blob/master/src/reticen8/mvc/app/views/layout_partials/form_input_tr.volt>`__ we offer some different record types which we will detail below:


**Attributes**

============  ===========================================================================================
Name          Description
============  ===========================================================================================
id            unique id of the attribute
type          type of input or field. For a list of valid types, use the Type table below
label         attribute label (visible text)
size          size (width in characters) attribute if applicable
height        height (length in characters) attribute if applicable
help          help text
advanced      property "is advanced", only display in advanced mode
hint          input control hint
style         css class(es) to add, helps identifying items easier using jQuery selectors
width         width in pixels if applicable
allownew      allow new items (for list) if applicable
readonly      if true, input fields will be readonly
============  ===========================================================================================


**Types**

==================  ===========================================================================================
Name                Description
==================  ===========================================================================================
header              Header row 
text                Single line of text
password            Password field for sensitive input. The contents will not be displayed.
textbox             Multiline text box
checkbox            Checkbox
dropdown            Single item selection from dropdown
select_multiple     Multiple item select from dropdown
hidden              Hidden fields not for user interaction
info                Static text (help icon, no input or editing)
==================  ===========================================================================================


---------------------
API based controllers
---------------------

For API calls a separate class is used to derive from, which implements
a simple interface to handle calls. The main difference with the view
controllers is that an action should return a named array containing
response data instead of picking a template.

A simple index controller to echo a request back looks like this:

.. code-block:: php

    class TestController extends ApiControllerBase
    {
        /**
         * @return array
         */
        public function echoAction()
        {
            if ($this->request->hasPost("message")) {
                $message = $this->request->getPost("message");
            } else {
                $message = " " ;
            }
     
            return array("message" => $message);
        }
    }

When placed inside the API directory of Vendor/Sample can be called by sending a
post request to /api/sample/test/echo, using jQuery:

.. code-block:: javascript

            $.ajax({
                type: "POST",
                url: "/api/sample/test/echo",
                success: function(data){
                    alert(data.message) ;
                },
                data:{message:"test message"}
            });


.. Tip::

    Reticen8 ships with two standard controllers to incorporate default action scenario's, such as mutating models
    and restarting services. These can be found in our repository `here <https://github.com/reticen8/core/blob/master/src/reticen8/mvc/app/controllers/Reticen8/Base/>`__
    and are named :code:`ApiMutableModelControllerBase`, :code:`ApiMutableServiceControllerBase`. Both extend :code:`ApiControllerBase`
    as described in this chapter. The mutable model controller is explained in more detail in :doc:`using grids <../examples/using_grids>`, the
    service controller is explained in :doc:`api enable services <../examples/api_enable_services>`
