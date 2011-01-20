## Preview

Make an ActiveRecord object preview-able, and display the preview using existing/custom templates  

## Install

    gem install preview

## Usage

### Within controller:  

    previewable  
This will enable preview generation for the resource that is handled by the controller (eg: post for PostsController)  

### Within view-form:

    f.preview  
Will generate a __preview__ button, on pressing which, the preview opens in a new tab.  
(f is the form object for the model.)  

## More options:   

    previewable :actions => [:mycreate]
The preview functionality works for forms that submit to the `mycreate` action, instead of the default (`create`, `update`)

    previewable :template => "myshow"  
The preview is generated using the _myshow.html.erb_ template instead of the default (_show.html.erb_)

## How it works:
When the form is submitted through the preview button, it sends all the form values to the create/update actions on the server. 
This gem adds a before_filter to those actions, where it creates the resource instance variable (@post for PostsController) using the passed values, and then renders the template using the instance variable.  

## Note:
The resource preview object is not persisted - no data is written to the database.