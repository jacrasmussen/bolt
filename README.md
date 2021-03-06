# Easier integrations for TYPO3 sites

This package is a TYPO3 extension that makes integration work easier.

We consider it best practice to run a site and all custom Backend Layouts, TypoScript, PageTS
in one place, a so-called "site extension". We prefix them with "site_" making it something like 
"site_myproject".

Then, the tricky part starts:
* Adding TypoScript
* Adding Fluid
* Adding PageTSconfig
* Adding Domains (for certain environments)

We want to avoid that for our sites, making life easier for integrators and get the website
up and running faster.

Because of this, this extension adds a field to the pages table (only for the records
marked as site root), where the integrator only selects his/her site package
and everything else is taken care of.

It's doing the same as you'd need to do manually all the time.

What you do:
* Create your site extension
* Install bolt, and choose your site extension on your root page
* Ensure your site extension contains one of the following files
    - Configuration/TypoScript/constants.txt or constants.typoscript
    - Configuration/TypoScript/setup.txt or setup.typoscript
    - Configuration/PageTs/main.tsconfig or Configuration/PageTsConfig/main.tsconfig

## When do I need this extension?

If you want to do one step less when developing a TYPO3 website :)

## How to install this extension?

You can set this up via composer (composer require cmsexperts/bolt) or via
TER (extension name "bolt"), it runs best with TYPO3 v8.

## License

The extension is licensed under GPL v2+, same as the TYPO3 Core.

For details see the LICENSE file in this repository.

## ToDo

- Kick start a site extension
- Deal with domains
- Add a integrator backend module to show the current setup
- Integrate Fluid templates, Content types, domain records, URL + language configuration
all in one place.
- Change the extension icon
- Make "disabling sys_template" optional
- Run all cases with extension templates / static inclusions work