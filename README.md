
#Client sample - ViewSaveAnimate

##Description

*This sample is part of the [Developer-Autodesk/Autodesk-View-and-Data-API-Samples](https://github.com/Developer-Autodesk/autodesk-view-and-data-api-samples) repository.*

This sample shows how you can save/restore views in the viewer and then replay them in a loop in specified order. The webpage is using a jQuery UI sortable component to store the views which are saved by user.
It enables you to 
* Drag&drop to sort the saved view buttons
* Drag buttons off the toolbar to remove them
* Switch to any saved view
* Animate the saved views

Buttons:
* "S": saves the current view. You can also use Alt+S to do the same
* "A": animates the stored views. It will start on the first view in the toolbar and keep switching to the next stored view until the last one is reached.
* "1".."n": the stored views

##Dependencies

You need other workflow samples to log in, upload a file, start translation to get required parameters.

##Setup/Usage Instructions

It requires the user to pass in a valid access token and urn of the file they want to use as a URL parameter:
* ViewSaveAnimate.html?accessToken=&lt;access token&gt;&urn=&lt;urn of the file to view&gt;
* e.g.: ViewSaveAnimate.html?accessToken=ljvWwXkzF3zxCVfLUZhP1Q8Qk66S&urn=dXJuOmFkc2sub2JqZWN0czpvcy5vYmplY3Q6bXl0ZXN0YnVja2V0L2NoYXNzaXMuZHdm

You can use e.g. the https://github.com/Developer-Autodesk/workflow-wpf-view.and.data.api sample to log in, upload a file, start translation and then invoke this html page with the required parameters. 

The html page has two parameters you can adjust:
* MyClass.kInBetweenSteps: this sets how many extra steps are added in between the stored views when animating, to make it smoother
* MyClass.kMilliSecondsBetweenSteps: the time in milliseconds that we'll wait before switching from one saved view to the next when animating

Note: in case of Firefox you'll need to disable the Alt menu toggle for Alt+S to work as Save View in this sample:
http://superuser.com/questions/770301/pentadactyl-how-to-disable-menu-bar-toggle-by-alt 

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.

##Written by 

Adam Nagy








