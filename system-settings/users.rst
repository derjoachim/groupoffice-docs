Users
=====

User management is available for administrators and any user who has permissions via System Settings -> Modules -> System permissions. 
When clicking users you will see a list of all Group-Office users. Via the "more"
menu in the record you can:

1. Edit the user
2. Login as this user
3. Archive a user
4. Delete the user

.. note:: Instead of deleting or archiving users you can simply disable them. Disabling a user will keep
   all data and references to the user but the user can't login or used for new items. To deactivate a
   user you must "Edit" it and toggle "Login enabled" on the account page.

.. warning::

.. figure:: /_static/system-settings/users.png
   :alt: User list

   User list

User defaults
-------------

Before adding any user. Check the 'User settings' to avoid unnecessary changes to 
user settings after creating them. 

Click the settings icon to change default values and manage custom fields.

.. figure:: /_static/system-settings/user-settings.png
   :alt: User settings

   User settings

Adding a user
-------------

.. note:: Before adding users make sure you've setup :ref:`user-groups` with the right
   module access. So setting up the user permissions is a simple matter of adding
   it to the right user group.

To add a user click the plus icon. A short wizard opens with three steps.

.. figure:: /_static/system-settings/create-user-1.png
   :alt: Create user step 1
   :width: 50%

   Create step 1

Supply the username, display name and e-mail address.

- Username is case insensitive.
- Display name is used in Group-Office
- Provide an account e-mail address. 
- Because often Group-Office is used as primary e-mail service you must provide
  a secondary e-mail address for e-mail recovery. If not available just use
  your primary e-mail.

.. figure:: /_static/system-settings/create-user-2.png
   :alt: Create user step 2
   :width: 50%

   Create step 2

Provide a password. You can also use the button in the first field top generate
a strong password.

.. figure:: /_static/system-settings/create-user-3.png
   :alt: Create user step 3
   :width: 50%

   Create step 3

Finally, add the user to the right :ref:`user-groups` andf click 'Finish'.

Edit a user
-----------

To edit a user double click or use the more menu. 
The edit dialog is identical to the ':ref:`my-account`' page but adds some administrative features:

- Group management
- Disable / enable login
- Set disk quota

Archiving a user
----------------

Archiving a user will not only disable the user. It will also hide any calendars, note books task lists and address books
from other non-admin users. If a user has updated their user profile, it is moved to a separate address book named 'Archived users'.
Additionally, all group memberships are revoked.

Although there is no explicit way to restore a user from the archive, an administrator can do this manually by performing the
following steps:

1. Re-enable the user by checking the 'Login enabled' checkbox.
2. Add the user to their relevant groups and save the user.
3. Move the user profile from the 'Archived' address to a more accessible one, e.g. 'Users'. This should be done from within the address book module.
4. Restore access to the user to their default address book, task list and note book.
5. If the projects-module is in use, you may need to re-add the user to the default resources for project templates.


Disk quota
``````````
If you leave this blank then users can use an unlimited amount of storage. If set
then the user will be limited to this amount of disk space.

Disk quota applies to all files in the user's home folder of the files module.
Other locations such as projects and address book folders are owned by the
"admin" user.

.. figure:: /_static/system-settings/my-account.png
   :width: 100%
   :alt: Edit user

   Edit user
   

.. _user-visibility:

Visibility of users
-------------------

By default all users are visible to each other. You can see users when you share something with another user for example.
If you'd like to change this you need to change the default permissions of a new user group. Because every user gets
it's own personal group used for permissions. You can change the default or at :ref:`user-groups-defaults`. It's also possible to reset or add new permissions for all users / groups at :ref:`user-groups-defaults` with the "Reset all" or "Add to all" buttons.

You can change visibility settings per user in the user account page at the "Visible to" tab.

.. note:: After an upgrade from 6.2 none of the users are visible. This is a known issue. If you'd like to make all
   users visible then edit the :ref:`default-permissions` of "Group" and add for example group "Everyone" and click
   "Add to all". Now all users can see all groups and users.
