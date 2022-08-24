## R4MVC


R4MVC is a Roslyn based code generator for ASP.NET MVC Core apps that creates strongly typed helpers that eliminate the use of literal strings in many places.  

It is a re-implementation of [T4MVC](https://github.com/enricosoft/R4MVC) for ASP.NET Core projects.

R4MVC runs in the dotnet cli or in Visual Studio 2017/2019/2022, and supports ASP.NET Core MVC 1 and 2

## Benefits

Instead of

````c#
@Html.ActionLink("Dinner Details", "Details", "Dinners", new { id = Model.DinnerID }, null)
````
R4MVC lets you write
````c#
@Html.ActionLink("Dinner Details", MVC.Dinners.Details(Model.DinnerID))
````

When you're using tag helpers, instead of
```html
<a asp-action="Details" asp-controller="Dinners" asp-route-id="@Model.DinnerID">Dinner Details</a>
```
you can write (after registering R4Mvc tag helpers in _ViewImports.cshtml with the directive: `@addTagHelper *, R4Mvc`)
```html
<a mvc-action="MVC.Dinners.Details(Model.DinnerID)">Dinner Details</a>
```

and that's just the beginning!

### Use the following links to get started

*   **Install** R4MVC is distributed using using [NuGet](http://nuget.org). Visit the [Installation page](https://github.com/enricosoft/R4MVC/wiki/Installation)
*   **Learn**: visit the [Documentation page](https://github.com/enricosoft/R4MVC/wiki/Documentation)
*   **Discuss**: Discuss it on [GitHub](https://github.com/enricosoft/R4MVC/issues)
*   **Contribute**
*   **History &amp; release notes**: [change history](CHANGELOG.md)
