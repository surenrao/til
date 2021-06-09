## dotnet 5
As of today (Jun-8-2021) when generating Dockerfile from VisualStudio 2019 for Asp.net core 5 SPA project, 
the default microsoft images dont include npm. So need to install nodejs. During development, install in asp image, and for building instal in sdk too.
example:

If the app uses System.Drawing or GDI inside linux container then we also need to install some libraraies.
example:
