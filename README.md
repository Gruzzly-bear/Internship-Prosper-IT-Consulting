# Live-Project-Summary

# Links
- [Image Cleanup](#Cleanup-of-image-edit-page)
- [Calander Issues](#Fixing-issues-with-the-calander)
- [Even page styling](#Stylizing-the-Event-add-page)
- [Debugging Javascript](#Debugging-Javascript)
- [Reformating code and design](#Reformatting-of-design-and-code)
- [Skills Acquired](#Other-skills-acquired)
- [Contact](#Contact-and-links)
## Introduction
I spent two weeks working on a live project with fellow students.
We developed a full scale MVC/MVVM Web Application in C#. A lot of the Application was developed and our main focus was improving the code, adding new features and fixing bugs. I was tasked with doing a mix of all of it. From fixing errors thrown by javascript, reformatting code, and even adding new features.

Although this was a live project worked on by a multitude of people, it was still for an actually and operating business. Therefore, I can only display snippits and rough mockups of what was done. I have created the mockups in the most simple form to give you an idea of what it looked like.

I'll list some of the stories I worked on and what I achieved along the way.



## Cleanup of image edit page
My first story was to clean up and re-arrange how the edit feature for images worked. This not only helped me understand Azure Dev-ops a bit more, but I was able to contribute something, albeit small. What I had done, was make it so that the image sizes themselves were displayed under each image dynamically. Automatically changing to match which ever image was selected.

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
<p align="center">
  <img width="460" height="300" src="https://i.imgur.com/43lYV5O.jpg">
</p>


<p align="center">
The way I accomplished this made it simple and understandable for the user to read.
</p>

## Fixing issues with the calander
There were a few issues with the calander that needed to be addressed. Such as checkboxes needing to be disabled when certain choices were chosen elsewhere. This was mostly useful for time selection of an event. There were two predetermined times in the system. Matinee and Evening. When ever someone selected the box for either of those, they wanted the dropdown selector for specific times to be disabled. Also, the same code could be reformatted and reused to disable the checkboxes if a specific time was checked in the checkboxes. The calander add event page needed to be cleaned and formatted to appeal better to the user. Everything was aligned to the left side of the page. Near to the edge. I adjusted some padding and centered everything.

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

<p align="center">
    Here is how it reacted when the drop down was selected.
</p>
<p align="center">
  <img width="460" height="300" src="https://i.imgur.com/AnlsqSM.jpg">
</p>



<p align="center">
Here is how it reacted when the Checkboxes were selected.
</P>
<p align="center">
  <img width="460" height="300" src="https://i.imgur.com/VcBlcxN.jpg">
</p>


## Stylizing the Event add page
Using bootstrap and various razer options, I was able to stylize and display the content in a more appealing way. With everything centered and place side by side, it not only appeared more asthetically pleasing on the eyes, but it was also more functional.


## Debugging Javascript
I was to figure out what was throwing exceptions on the application. Bugs are a huge annoyance and even the smallest and easiest ones to squash, are hard to find. After looking through the code and doing a bit of research I was able to locate where the issues were and correct them. 

### The first Error was "Uncaught ReferenceError: $ is not defined".
This normally happens when a custom script is loaded before jquery is called in the file itself.
This was fixed by simply moving how the scripts were loaded on the page.

### The second erorr was Uncaught SyntaxError: Identifier ~~'XXXXXXXXX'~~ has already been declared.
This happens when a varieble with strict proerties has been called already.
This was was resolved by putting a section of code containing the varieble into braces.

## Reformatting of design and code
I reformatted multiple instances of code to not only make it look better on the front end, but to make it easier to read for the devs as well. This involved thinks like, centering code for readability, A cleaner appearance and look, and overall quality. I also reformatted and refactored code to make it easier for other developers working on the project.

## Other skills acquired
- The ability to comfortably work on a project and utilize Azure Dev-ops to successfully publish the code efficiently.
- To help an assist other developers with their projects.
- Look into problems I don't initially know and figure out how to solve them efficiently.
- Work with a team of other developers.
  - Share ideas and constructive criticism effectively and efficiantly. Learning off of eachother's experiences and knowledge.
  - Work in tandem with other developers to insure that everything goes smoothly.

## Contact and links
- [Github](https://github.com/Gruzzly-bear)
- [Email](mailto:gruzzly-bear@outlook.com?subject=Hey%20There!)
- [Website](https://gruzzly.co)
