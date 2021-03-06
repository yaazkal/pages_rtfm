---
title: TITLE
slug: URI
menu: MENU
date: 08-08-2016
published: true
visible: true
taxonomy:
    category: docs
routes:
    aliases:
        - /URI
---

How to Manage Aliases and Redirects

When you create a site in Aegir, there is a textarea where you can
enter aliases and a checkbox to set whether these aliases should
redirect to the main domain. Once the site is created, you can access
these settings again by clicking the @Edit@ tab.

h2. Task: Edit Aliases and Redirects

To edit the aliases and redirects for a site, *click the @Edit@ tab*
in the upper left.

On the Edit screen, you can add or remove aliases in the large
@Domain aliases@ textarea.

To make all these aliases into redirects, check @Redirect domain
aliases to the main domain@.

h2. Task: Redirect to "www."

If you want your main domain to begin with "@www.@", you may need to
take an extra step.

If you are creating the site, no extra step is needed. Simply enter
the @www.@ domain as the main domain. For instance, you could enter
@www.foo.com@.  Aegir will add @foo.com@ as an alias _automatically_.

However, if you already created the site as @foo.com@, you cannot
@Migrate@ it to @www.foo.com@ directly. Aegir has already created
@www.foo.com@ as an alias.

Instead:

# Use the @Migrate@ task to move the site to some other domain,
such as @anything.foo.com@.

# Then @Migrate@ the site to @www.foo.com@.

# Finally, set the checkbox to enable redirects. Now a visit to
  @foo.com@ will cause a 301 redirect to @www.foo.com@.

h2. More Information

h3. Can You Use .htaccess for Redirects?

*No.* Aegir and "Nginx":nginx have no .htaccess file.  You must use
the Aegir interface to manage your Nginx redirects.

If you need specialized aliases which cannot be created in this
interface (for instance, using regular expressions), contact
"support":support.

[nginx]
