# NuGet Helpers

## Packaging for local use

Add the following property group to your project

```xml
<PropertyGroup>
  <PackageId>HelloWorldApiSpecification</PackageId>
  <Version>1.0.0</Version>
  <Authors>Tony</Authors>
  <Company>Tonys-Stuff</Company>
  <GenerateAppxPackageOnBuild>true</GenerateAppxPackageOnBuild>
</PropertyGroup>
```

Package from the project directory using

```powershell
dotnet pack
```

A `nupkg` file will be created in the project `bin` folder somewhere!

Create a local feed which is just a folder to store the packages. I usually use `c:\d\tonys-nuget-feed`

Now add the package to the feed.

```powershell
nuget add "c:\project\bin\etc\mynugetpackage.nupkg" -Source c:\d\tonys-nuget-feed
```

Now with VS you can add the feed that points to `c:\d\tonys-nuget-feed` and install your packages from this feed