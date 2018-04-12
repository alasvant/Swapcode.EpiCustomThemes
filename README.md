# Swapcode.EpiCustomThemes
Episerver sample theme for admin view. Affects only the Episerver admin views.
Basically increases the font size for readability. Demonstrates switching of default button icons. Adds padding to table headers and rows (also fixes align="center" usage with CSS style, so content is actually aligned center).

# Changes versus the Default theme
Look at the ToolButton.less and system.css files, there are comments 'modified' that you can search in the files to see the changes. Other option is to use [WinMerge](http://winmerge.org/) or similiar tool to compare the files ;)

# Install
Add my public MyGet feed to Visual Studio package sources:
- NuGet v3 (VS2015+): `https://www.myget.org/F/swapcode-episerver/api/v3/index.json`
- NuGet v2 (VS2012+): `https://www.myget.org/F/swapcode-episerver/api/v2`

Install using package manager UI in Visual Studio or in Package Manager Console:
`Install-Package Swapcode.EpiCustomThemes -Version 1.0.0 -Source https://www.myget.org/F/swapcode-episerver/api/v3/index.json`

MyGet: [Swapcode.EpiCustomThemes](https://www.myget.org/feed/swapcode-episerver/package/nuget/Swapcode.EpiCustomThemes)

# Configuration
The package does no modifications so you need to manually change your Episerver configuration.
Locate in web.config your episerver applicationSettings element and add attribute (or edit existing):
`uiTheme="SCRefresh"`
This will make Episerver use this custom theme.

# Copyrights etc
Please do note that I do not own any copyrights to the content, it is derived from Episerver content.
The source folder [Default](https://github.com/alasvant/Swapcode.EpiCustomThemes/tree/master/Default) contains the Episerver original content.

The modified icons are taken from [Find Icons](https://findicons.com/) and only free and no license link required icons were used.

# Creating NuGet package
Increase the version number in nuspec file and the run command:
`nuget pack Swapcode.EpiCustomThemes.nuspec`
