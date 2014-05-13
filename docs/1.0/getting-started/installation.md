# Installation

Courses is an app built on top of the [Elefant CMS](http://www.elefantcms.com/download) platform.
Follow the steps on the Elefant website to get the base CMS up and running,
then follow these steps to install Courses:

1\. From the root folder of the site, run the following command:

	php composer.phar require elefant/app-courses

This will also install the following apps that Courses depends on:

* [Comments](https://github.com/jbroadway/comments)
* [SCORM](https://github.com/jbroadway/scorm)
* [Stripe Payments](https://github.com/jbroadway/stripe)

> **Note:** You may need to add `"minimum-stability": "dev"` to your `composer.json`
> file in order for Composer to work correctly while Courses is still in development.

> **Payments:** Additional payment providers can be supported by implementing the
> [payment handler interface found here](https://github.com/jbroadway/stripe#creating-a-member-payment-or-subscription-form).
> More documentation and examples still to come.

2\. Log into Elefant and run the Courses installer by navigating to Tools > Courses.

3\. Add the following line to the `[Hooks]` section of `conf/config.php` to enable
email notifications of comments to course instructors:

```
comments/add[] = courses/hook/comments
```

4\. Go to Tools > Navigation and add the `Courses` page to your site tree.

You should now have a working installation.

Next: [[:Support]]