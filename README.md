## Live-Project-Summary

# Introduction
The final two weeks at the tech academy was spent working on a live project with fellow students. 
We developed a full scale MVC/MVVM Web Application in C#. A lot of the Application was developed and our main focus was improving the code, adding new features and fixing bugs. 
I'll list some of the stories I worked on and what I achieved along the way.



# Cleanup of image edit page
My first story was to clean up and re-arrange how the edit feature for images worked. This not only helped me understand Azure Dev-ops a bit more, but I was able to contribute something, albiet small.

```csharp
    <div class="form-group">
        <img class="medium_size" src='@Url.Action("DisplayPhoto", "Photo", new { id = Model.PhotoId })' />
        <br />
        <p class="strong">Height :  @Html.DisplayFor(model => model.OriginalHeight)
            px | Width : @Html.DisplayFor(model => model.OriginalWidth) px</p>
        @*@Html.LabelFor(model => model.PhotoFile, htmlAttributes: 
        new { @class = "control-label col-md-4 inputLabel" })
    </div>
```

The way I did it made it simple and understandable for the user to read.