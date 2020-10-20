# How to build and make changes to the site [![pipeline status](https://gitlab.com/zurech/EstudioAgrimensorRoldan/PromotionWebPage/badges/master/pipeline.svg)](https://gitlab.com/zurech/EstudioAgrimensorRoldan/PromotionWebPage/-/commits/master)

## Clone gitlab repository

`git clone git@gitlab.com:zurech/EstudioAgrimensorRoldan/PromotionWebPage.git`

## Pre-requisites

* [Git](https://git-scm.com/)

## Test changes locally

Modify `html`, `css` and `js` files and test the changes locally opening the site in your local computer in a web browser such as Chrome or Firefox.

## Test changes in DEV environment (Gitlab Pages)

Once changes are rewied locally it is time to move those changes to the DEV Environment.

To do so, next steps must be followed:

* Before making changes explained in the previous section, a feature branch must be checked out from master branch:

    ```git checkout master```

    ```git checkout -b <feature_branch>```

* Once the changes are tested and commited locally, upload the changes to GitLab Server:

    ```git push origin <feature_branch>```
    
* After pushing the feature branch to Gitlab an automatic pipeline will be trigered in order to upload the changes into Gitlab Pages. Once the pipeline has finished successfully changes can be reviewed in the following link: [https://zurech.gitlab.io/EstudioAgrimensorRoldan/PromotionWebPage](https://zurech.gitlab.io/EstudioAgrimensorRoldan/PromotionWebPage)


* If you are confortable with the changes then a MR can be created in order to merge the changes into the master branch.

## Move changes to Production (AWS S3)

Once changes are approved in DEV Environment and merged into master branch another pipeline will be triggered automatically in order to upload changes to the Production site in AWS. Once the pipeline has finished successfuly changes can be reviewed in the following link:

* [http://www.roldanagrimensura.com.ar/](http://www.roldanagrimensura.com.ar/)