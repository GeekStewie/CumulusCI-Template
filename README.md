# CumulusCI-Template

This is an example template repo for use with Solution Development using CumulusCI and Salesforce DX

## Initial Environment Setup

To work on this project in a scratch org:

1. [Set up CumulusCI](https://cumulusci.readthedocs.io/en/latest/tutorial.html)
2. [Set up Playwright](https://cumulusci.readthedocs.io/en/latest/robot-playwright.html)

## Development Steps

To work on this project in a scratch org:

1. Create a new scratch org called dev
2. Create a new scratch org called qa
3. Run `cci flow run deploy_solution --org dev` to deploy this project to dev. Run `cci org browser dev` to open the org in your browser.
4. Make changes in Salesforce org
5. Capture Changes from org using `cci task run retrieve_changes --org orgalias` replacing "orgalias" with the alias of the target org, e.g. dev or qa
6. Test deploy changes to QA org, `cci flow run deploy_solution --org qa`
7. Repeat steps 5-6 until successful deployment
8. Save changes back to Github

## CI/CD

See this article for more information on how to set this up within your repo - [Set Up GitHub Actions](https://cumulusci.readthedocs.io/en/latest/github-actions.html)

## Thanks

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.paypal.com/paypalme/geekstewie?country.x=GB&locale.x=en_GB)
