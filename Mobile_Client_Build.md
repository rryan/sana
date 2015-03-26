# Sana Mobile Android Client #

---

## Overview ##
The new client code is intended to be a self-contained, modularized, project including all necessary support libraries and unit testing code.

## Contents ##
  * **api** - Pure Java library consisting of POJO's and code w/o Android    dependencies
  * **api-android** - Common library for Sana mobile Android client as well external plugin apps.
  * **app-android** - Sana mobile client
  * **libs** - Additional libraries required by the projects.

## Development Requirements ##

---

  1. Git
  1. JDK(latest 1.6 release)
  1. Android ADT Bundle
> > http://developer.android.com/sdk/index.html
  1. Android Support Library(Install using SDK manager)
> > http://developer.android.com/tools/support-library/setup.html
  1. Add API 7 and 16 using SDK manager
  1. Android virtual device, or phone which supports API 7 or greater

## Code installation instructions ##

---

  1. Start Eclipse bundled with ADT
  1. Import the sana code projects:
    1. Navigate to **File --> Import --> Git --> Projects from Git**
    1. Use the following URI for import
> > > https://code.google.com/p/sana.mobile/
    1. Select all branches
    1. Use defaults for local destination
    1. Select all of the projects
      * **api**
      * **api-android**
      * **app-android**
      * **app-android-tests**
  1. Import the **android-support-v7-appcompat** project into your workspace. The sana.mobile Android code assumes it has been copied into the workspace. If you do not copy you will need to update the library reference later. Some problems have been reported if the Add **android-support-v7-appcompat** project is set to build automatically.
    1. Add the following to the Java Build Path
      * **android-support-v4.jar**
      * **android-support-v7-appcompat.jar**
    1. Select Android Private Libraries in Export tab of Java build path For more info, refer to:
> > > http://developer.android.com/tools/support-library/setup.html#libs-with-res

## Troubleshooting ##

---

  1. Missing Android dependencies. Use the "Android SDK Manager" to add any missing API levels. In Eclipse, it can be launched by selecting "Window --> Android SDK Manager"
  1. **NoClassDefFoundError** when running the client application. By default, the ADT plugin does not export libraries included in the build. To correct this issue, right click on the project in Eclipse and open the Properties window. Select: **Java Build Path --> Order and Export**
  1. Path issues with v7-appcompat library reference in api-android. Right click on the project and select **Properties --> Android** and check the Library references at the bottom of the window. A large red x by the v7-appcompat indicates the path needs to be corrected. You may need remove and re-add the appcompat project from your workspace.