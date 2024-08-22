## aft-sample-global-customizations

Sample repository and customization for AWS Control Tower Account Factory for Terraform (AFT).

This repository is part of AFT lab. For detailed walkthrough, please check the lab in [AWS Control Tower Workshop](https://catalog.workshops.aws/control-tower/en-US/customization/aft).

## How to use 

There are four repository, to help you get started:
- [aft-sample-account-provisioning-customizations](https://github.com/aws-samples/aft-sample-account-provisioning-customizations)
- [aft-sample-account-customizations](https://github.com/aws-samples/aft-sample-account-provisioning-customizations)
- [aft-sample-global-customizations](https://github.com/aws-samples/aft-sample-global-customizations)
- [aft-sample-account-request](https://github.com/aws-samples/aft-sample-account-request)

Refer to instruction on [AWS Control Tower Workshop](https://catalog.workshops.aws/control-tower/en-US/customization/aft/) for detailed walkthrough.

## How to use

This is sample repository for `aft-global-customizations`. 

For the labs in the workshop we deploy AFT using GitHub as our vcs provider.
- Open the `aft-sample-global-customizations` in your browser 
 - Click on the **Fork** button,
 - Edit the name of repository to be `aft-global-customizations`.
 - Ensure **Copy the main branch only** is checked.
 - Select **Create fork**
 - Check that the repository you've created is marked as **Private**

If you are doing AFT for production use, you may select on of the other [VCS providers supported by AFT](https://docs.aws.amazon.com/controltower/latest/userguide/aft-alternative-vcs.html).
- If you would rather create an entirely isolated repository (rather than forking), then you can down load the content in a zip file and then unpack it into the equivolent repository in you environment.
 - Open the `aft-sample-global-customizations` in your browser
   - Click **Code**, **Download ZIP**
   - note where your browser saved the download it will be named something like `aft-sample-global-customizations-main.zip`
 - Create the repository in you environment `aft-global-customizations`
   - If necessary clone the repository to a system from which you can commit and push to the repository.
   - unpack the zip downloaded above into the local repository.
   - Follow you normal processes for committing changes to a repository in your environment.

It is an AWS best practice to have multiple environments for workloads/applications to allow though testing before making changes to your production environment. This also applies to AWS Control Tower and Account Facotry for Terraform (AFT). So it is worth thinking about how you different environments are going to be connected to their repositories.

Will you use separate branches and merge requests to promote changes between environments?

or 

Will you have non-production repositories forked from your production ones and use a pull request approach?

With either strategy, it is unlikely you would want to replicate all of the accounts you require in your production environment in your testing one. For this reason is is recommended you have an instance of `aft-sample-account-request` per environment.

For example:
- `aft-account-request-sandbox`
- `aft-account-request-production`

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

