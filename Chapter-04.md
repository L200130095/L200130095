# Users, permissions, and roles

Every visitor to your site, whether they have an account and log in or visit the site anonymously, is considered a user to Drupal. Each user has a numeric user ID, and non-anonymous users also have a user name and an email address. Other information can also be associated with users by modules; for instance, if you use the core Profile module, you can define user profile fields to be associated with each user.

Anonymous users have a user ID of zero (0). The user with user ID one (1), which is the user account you create when you install Drupal, is special: that user has permission to do absolutely everything on the site.

Other users on your site can be assigned permissions via roles. To do this, you first need to create a role, which you might call "Content editor" or "Member". Next, you will assign permissions to that role, to tell Drupal what that role can and can't do on the site. Finally, you will grant certain users on your site your new role, which will mean that when those users are logged in, Drupal will let them do the actions you gave that role permission to do.

You can also assign permissions for the special built-in roles of "anonymous user" (a user who is not logged in) and "authenticated user" (a user who is logged in, with no special role assignments). Drupal permissions are quite flexible—you are allowed to assign permission for any task to any role, depending on the needs of your site.

Read more about this topic in The Drupal Cookbook (for beginners).

# Content types

A single web site could contain many types of content, such as informational pages, news items, polls, blog posts, real estate listings, etc. In Drupal, each item of content is called a node, and each node belongs to a single content type, which defines various default settings for nodes of that type, such as whether the node is published automatically and whether comments are permitted. (Note that in previous versions of Drupal, content types were known as node types.)

When you first install Drupal with the default installation profile (in contrast to the minimal installation profile), you will have two content types defined: "Article" and "Basic page". When you enable other core and contributed modules (by visiting Modules), you will find that you have other content types available; you can also create your own content types (see below).

## Content types in Drupal 7 and 8

### Article

The Article content type (formerly, "story") is enabled in Drupal in the default installation profile. Articles are generally used for information that is updated more frequently and often cross-referenced and categorized (such as news items or resources). By default, Articles are sorted with the most recent post at the top, but this can be customized with contributed modules like Views.

### Basic page

The Basic page content type is enabled in Drupal in the default installation profile. Typically Basic pages are used for static content that can (but are not required to) be linked into the main navigation bar.

### Book Page

Book pages are designed to be part of a collaborative book, enabled by the core Book module. An example of a collaborative book is the Drupal developer documentation. In older versions of Drupal, only nodes of content type Book Page could be added to a book. However, since Drupal 7 nodes of any content type can be part of a book.

### Forum topic

A Forum topic defines a topic for a forum discussion; people can reply to the topic by using comments. Forum nodes are organized into subject areas via a Taxonomy (list of categories).

## Poll

A poll is a question with a set of possible responses. Once created, a poll automatically provides a simple running count of the number of votes received for each response.

## Your own(Custom Content Type)

You can create your own custom content types by going to ` Menu > Structure > Content types > Add content type (admin/structure/types/add)`. You might do this as a way to organize your content. For instance, you might have "Info" and "News flash" as two simple content types on your site, rather than just using "Article" for both.
Content types by contributed modules

Finally, contributed modules define their own content types. Check the [Download & Extend/Modules page](https://www.drupal.org/project/project_module) of the Drupal handbook for more information on locating an appropriate module for your needs.

## Content types in Drupal 5 and Drupal 6

As mentioned above, the default content types in Drupal 5 and 6 are Story and Page. Field management is included in Drupal 7 & 8's core content types. If you want to add custom fields to your content types in Drupal 5 or 6, install the Content Construction Kit (CCK) contributed module. Custom fields are used to store additional information beyond the Drupal defaults (title, body, authoring information, time created/updated, and publishing status); for instance, on a real estate site, a real estate listing content type might have fields for the type of property, land area, etc. Additional information on the CCK module is available from the Content Construction Kit Handbook.

## Blog Entry

The Blog (short for weblog) content type was removed in Drupal 8. It is an online journal or diary, and Blog module allows registered users on your site to create their own blogs. Each entry in a user blog has content type Blog Entry.


# In Drupal, viewing a page and editing a page are almost the same

Occasionally, people who have previously used other editors (FrontPage, Dreamweaver) or CMS's (Joomla, etc.) ask how they access the admin area or "back-end" of Drupal. Sometimes they ask how they can preview their changes and see the "front-end".

* In Drupal, there is no such distinction, it just provides a unified interface.
* If (as an administrator, themer, or coder) you are looking at the homepage of your website, you are previewing it from the perspective of that role. Log out and you get the full 'anonymous' experience.
* Drupal usually looks pretty much the same to anonymous browsers as it does to editors, only with different features and menu items available.
* Authenticated users, with appropriate permissions, will see the 'edit' tabs above their pages. That's often the only difference between editor and user experience.

We find that people who have never used a CMS before are often much less confused about this approach than people who have previously used systems where the 'input' screens look totally different from the 'output' screens, according to the Drupal usability tests from the University of Baltimore in 2008. It's an un-learning thing.

However, if you want, you can still set an 'Administration theme' (in the settings Administer › Site configuration > Administration theme ) so that your admin pages look different from the front end. ... It still actually behaves the same way, but it may help if your public presentation theme is highly graphic or stylized.

Examples:

![Page as viewed by an editor (in Drupal 8).](https://www.drupal.org/files/un-declariation-human-rights-editor.png)

> Figure 4.1. Page as viewed by an editor (in Drupal 8).

![Page viewed as an anonymous visitor (in Drupal 8).](https://www.drupal.org/files/un-declariation-human-rights-anonymous.png)

> Figure 4.2. Page viewed as an anonymous visitor (in Drupal 8).



