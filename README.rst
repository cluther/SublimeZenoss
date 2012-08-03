SublimeZenoss
=============================================================================

This is a `Sublime Text 2 <http://www.sublimetext.com/2>`_ package that intends
to make `Zenoss <http://www.zenoss.com/>`_ ZenPack development easier.

This package contains the following tab triggered snippets:

* XML (or ZCML) files:

  * zconfigure

    Generates a full boilerplate configure.zcml for your ZenPack. The following
    fields can then be set:

    1. `shortname`: Usually a lowercase representation of the ZenPack's name.

    2. `ShortClassName`: A Python class-friendly capitalization of `shortname`.

    3. `DeviceClassName`: The Python class name of any custom Device subclass
       contributed by the ZenPack.

  * zcopyright

    Adds the standard XML copyright header. By default it copyrights to Zenoss,
    Inc. So as you might imagine, it's more useful for Zenoss employees.

* Python files:

  * zdevice

    Generates a full boilerplate for a Device subclass contributed by the
    ZenPack including the model class and the API interfaces and wiring.

    The following fields can be set:

    1. `ClassName`: Name of the Device subclass.

    2. `attribute`: Name of the first attribute for the class.

    3. `string`: Type for the `attribute`.

    4. `Attribute`: Friendly capitalized title for the `attribute`. Used in the
       user interface.

    5. `TextLine`: Zope schema type for the `attribute`.

  * zcomponent

    Generates a full boilerplate for a DeviceComponent subclass contributed by
    the ZenPack including the model class and the API interfaces and wiring.

    The fields are the same as for `zdevice` above.

  * zcopyright

    Adds the standard Python copyright header. By default it copyrights to
    Zenoss, Inc. So as you might imagine, it's more useful for Zenoss
    employees.

* JavaScript files:

  * zjs

    Generates a simple anonymous function to prevent your ZenPack from
    interfering with the global scope. Also defines a `ZC` variable for easy
    access to the `Zenoss.component` namespace.

  * zcomponent

    Generates boilerplate required to create a custom user interface for a
    DeviceComponent subclass. This includes the human-friendly name
    registration and custom component grid panel.

    The following fields can be set:

    1. `MetaType`: The meta_type for the related DeviceComponent subclass. This
       is the same as `ClassName` from the Python `zcomponent` snippet.

    2. `Singular Name`: A human-friendly name for the component type in a
       singular context.

    3. `Plural Name`: A human-friendly name for the component type in a plural
       context.

    4. `attribute`: Name of the first attribute for the component. This is the
       same as `attribute` from the Python `zcomponent` snippet.

    5. `Attribute`: Friendly capitalized title for the `attribute`. This is
       used as the column header for the attribute.

  * zcopyright

    Adds the standard JavaScript copyright header. By default it copyrights to
    Zenoss, Inc. So as you might imagine, it's more useful for Zenoss
    employees.


Installing
-----------------------------------------------------------------------------

With Package Control
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The easiest way to install `SublimeZenoss` is through `Package Control
<http://wbond.net/sublime_packages/package_control>`_.

Once you install Package Control, restart ST2 and bring up the Command Palette
(``Command+Shift+P`` on OS X, ``Control+Shift+P`` on Linux/Windows). Select
"Package Control: Install Package", wait while Package Control fetches the
latest package list, then select Zenoss when the list appears. The advantage of
using this method is that Package Control will automatically keep
SublimeZenoss up to date with the latest version.

With Git
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Clone the repository in your Sublime Text 2 Packages directory, located
somewhere in user's "Home" directory::

    git clone git://github.com/cluther/SublimeZenoss.git


Without Git
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Download the latest source from `GitHub
<http://github.com/cluther/SublimeZenoss>`_ and copy the whole directory into
the Packages directory.

The "Packages" packages directory is located at:

* OS X::

    ~/Library/Application Support/Sublime Text 2/Packages/

* Linux::

    ~/.Sublime Text 2/Packages/

* Windows::

    %APPDATA%/Sublime Text 2/Packages/
