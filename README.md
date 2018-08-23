# SqlLocalDB2016-Bootstrapper
ClickOnce and Visual Studio Installer bootstrapper package for Microsoft SQL Server 2016 Express LocalDB.

**To use:**

Clone the repository to your computer or download and extract one of the attached archives from the latest release. 
Copy the whole `SqlLocalDB2016` folder to the bootstrapper `Packages` folder, e.g. `C:\Program Files (x86)\Microsoft Visual Studio [VS_Version]\SDK\Bootstrapper\Packages`. 

Latest Visual Studios changed that folder location to something like `C:\Program Files (x86)\Microsoft SDKs\ClickOnce Bootstrapper\Packages`
The path to this folder can be found in the registry in the `Path` value from the following registry key (where `14.0` should be replaced with the Visual Studio version you're using):

> HKLM\Software\Microsoft\GenericBootstrapper\[VS_Version]

or, for x64 Windows:

> HKLM\Software\Wow6432Node\Microsoft\GenericBootstrapper\[VS_Version]

The packge should then be shown in Visual Studio along with other bootstrapper packages. If you want to provide the component together with your application rather than downloading from Microsoft then you'll also need to download the two `sqllocaldb.msi` files specified in the `package.xml` file for the region and save them in the `SqlLocalDB2014` folder, renamed to `SqlLocalDB.msi`.
