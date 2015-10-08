# Is Drupal the right tool for the job?

Drupal is a powerful and flexible content management system for building virtually any kind of website. Here are some examples of projects Drupal would work well for.

* You need a site that is flexible enough to evolve in any direction. For example, you might start with a blog but might want the option of adding other features like a wiki, electronic commerce, forums, multiple content types, etc.
* You need a site that can easily be configured to interact with other sites or with other technologies.
* You need a site that can easily handle complex forms and workflows.
* You need the ability to create your own content types. For example, you need to add a custom field to a page.
* You need the ability to quickly organize and display lists of information.
* You have needs that would be addressed by one of over 16,000 Drupal modules.
* You need to quickly develop custom functionality.
* You need to create web applications and mashups using third party APIs.

On the other hand, for certain limited uses, Drupal may not be the best choice:

* `If your only requirement is to write a personal blog`, you may want to consider using a more specialized blogging platform like WordPress or a hosted blogging solution like Blogger. Although Drupal can serve as a blogging platform out-of-the-box, blog-specific software may have a simpler administration interface and allow for easier customization and posting.
* Similarly, `if your only requirement is to create a wiki`, you should probably consider using dedicated wiki software like MediaWiki or a hosted wiki solution. You can certainly configure Drupal so that anyone can edit content (and even enable advanced wiki features with the help of several contributed modules like wikitools and Diff), but it may be simpler for you to use a more specialized solution.
* `If your only requirement is to host discussion forums`, you will want to consider a system such as SimpleMachines or phpBB with a mature set of Forum features, or Vanilla which has many plug-ins. If you need a custom forum, however, Drupal's forum module with forum enhancement modules like Advanced Forum may be better suited to extension.

`Important note`: When evaluating any software the user should always do due diligence and ensure that the software is properly maintained with regular security fixes and updates. Drupal.org is not responsible for any of the above software hosted on external websites. For more about Drupal security see this page.

With every release, Drupal is becoming easier to use; but like most powerful tools, it will always have a learning curve. Drupal takes time and commitment to learn how to use, and if you or your organization are not prepared to spend some time learning how Drupal works (or if you are not able to hire Drupal expertise), it may not be your best option.


## Users, permissions, and roles

Every visitor to your site, whether they have an account and log in or visit the site anonymously, is considered a user to Drupal. Each user has a numeric user ID, and non-anonymous users also have a user name and an email address. Other information can also be associated with users by modules; for instance, if you use the core Profile module, you can define user profile fields to be associated with each user.

Anonymous users have a user ID of zero (0). The user with user ID one (1), which is the user account you create when you install Drupal, is special: that user has permission to do absolutely everything on the site.

Other users on your site can be assigned permissions via roles. To do this, you first need to create a role, which you might call "Content editor" or "Member". Next, you will assign permissions to that role, to tell Drupal what that role can and can't do on the site. Finally, you will grant certain users on your site your new role, which will mean that when those users are logged in, Drupal will let them do the actions you gave that role permission to do.

You can also assign permissions for the special built-in roles of "anonymous user" (a user who is not logged in) and "authenticated user" (a user who is logged in, with no special role assignments). Drupal permissions are quite flexible—you are allowed to assign permission for any task to any role, depending on the needs of your site.

Read more about this topic in The Drupal Cookbook (for beginners).


