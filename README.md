# Live-Project-Summary

# Links
- [Image Cleanup](#Cleanup-of-image-edit-page)
- [Debugging Javascript](#Debugging-Javascript)
- [Skills Acquired](#Other-skills-acquired)
- [Contact](#Contact-and-links)
## Introduction
The final two weeks at the tech academy was spent working on a live project with fellow students. 
We developed a full scale MVC/MVVM Web Application in C#. A lot of the Application was developed and our main focus was improving the code, adding new features and fixing bugs. 
I'll list some of the stories I worked on and what I achieved along the way.



## Cleanup of image edit page
My first story was to clean up and re-arrange how the edit feature for images worked. This not only helped me understand Azure Dev-ops a bit more, but I was able to contribute something, albeit small.

```csharp
    <div class="form-group">
        <img class="medium_size" src='@Url.Action("DisplayPhoto", "Photo", new { id = Model.PhotoId })' />
        <br />
        <p class="font-weight-bolder lead">Height :  @Html.DisplayFor(model => model.OriginalHeight)
        px | Width : @Html.DisplayFor(model => model.OriginalWidth) px</p>
        @*@Html.LabelFor(model => model.PhotoFile, htmlAttributes: 
        new { @class = "control-label col-md-4 inputLabel" })
    </div>
```

The way I did it made it simple and understandable for the user to read.

## Fixing issue with the calander.
There were a few issues with the calander that needed to be addressed. Such as checkboxes needing to be disabled when certain choices were chosen elsewhere.

```Javascript
    $('#disableUnchecked').change(function () {
        if ($(this).is('select')) {
            // disable the dropdown:
            $('#event').attr('disabled', 'disabled');
        } else {
            $('#event').removeAttr('disabled');
        }
    });
```
## Stylizing the Event add page.
Using bootstrap and various razer options, I was able to stylize and display the content in a more appealing way.


## Debugging Javascript
I was to figure out what was throwing exceptions on the application. Bugs are a huge annoyance and even the smallest and easiest ones to squash, are hard to find. After looking through the code and doing a bit of research I was able to locate where the issues were and correct them. 

### The first Error was "Uncaught ReferenceError: $ is not defined".
This was fixed by simply moving how the scripts were loaded on the page.

### The second erorr was Uncaught SyntaxError: Identifier ~~'XXXXXXXXX'~~ has already been declared.
This was was resolved by putting a section of code into braces.

## Other skills acquired
- The ability to comfortably work on a project and utilize Azure Dev-ops to successfully publish the code efficiently.
- To help an assist other developers with their projects.
- Placeholder
- Team building Placeholder
  - Placeholder
  - Placeholder

## Contact and links
- [Github](https://github.com/Gruzzly-bear)
- [Email](mailto:gruzzly-bear@outlook.com?subject=Hey%20There!)
