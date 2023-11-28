# Hello , Packer

- where the `Hashicorp  packer` fits in the `hashicorp Suite for tools`

- we have below `hashicorp tool` which is available for both `open souirce and enterprize version`
  
  - `Hashicorp Terraform `
  
  - `Hashicorp Vault`
  
  - `Hashicorp Consul`
  
  - `Hashicorp Nomad`
  
  
- we have the `below hashicorp tools` which is available in `only in opensource`
  
  - `Hashicorp Waypoint` :- came in hashicorp 2020
  
  - `Hashicorp Boundary` :- came in hashicorp 2020
  
  - `Hashicorp Packer`
  
  - `Hashicorp Vagrant` 


# What is HashiCorp Packer?

  - `hashicorp packer `is a `Open-Source Machine Image Creation Tool`
  
  - `hashicorp packer` will help us in `automate` the `installation` `configuration` of `packer made images`
  
  - we learned that `we will be taking the base image` that `we created or provided by cloud provider` , we can customize that `base image` and `create new image` using `packer`
  
  - `Hashicorp Packer` Works with `Multiple Platforms` – `Even from the Same packer template Configuration`
  # Hello , Packer

- where the `Hashicorp  packer` fits in the `hashicorp Suite for tools`

- we have below `hashicorp tool` which is available for both `open souirce and enterprize version`
  
  - `Hashicorp Terraform `
  
  - `Hashicorp Vault`
  
  - `Hashicorp Consul`
  
  - `Hashicorp Nomad`
  
  
- we have the `below hashicorp tools` which is available in `only in opensource`
  
  - `Hashicorp Waypoint` :- came in hashicorp 2020
  
  - `Hashicorp Boundary` :- came in hashicorp 2020
  
  - `Hashicorp Packer`
  
  - `Hashicorp Vagrant` 


# What is HashiCorp Packer?

  - hashicorp packer is a `Open-Source Machine Image Creation Tool`
  
  - `hashicorp packer` will help us in `automate` the `installation` `configuration` of `packer made images`
  
  - we learned that `we will be taking the base image` that `we created or provided by cloud provider` , we can customize that `base image` and `create new image` using `packer`
  
  - `Hashicorp Packer` Works with `Multiple Platforms` – `Even from the Same packer template Configuration`
  
  - if we have running on both `AWS and Azure` we can have the `single template` `which build out the image on both the platform in a single run` 
  
  - using this `single packer template` we can `maintain the consistency` accross the `multiple platform` using the `single packer build`
  
  - `hashicorp packer` ultimate goal is to help in `eleminate`  all the `manual step` that we have to do `in order to create the golden image` which can used accross `multiple platform`
  
  - if we wgo to `AWS/Azure/VMware` wherever ,a lot of times there are multiple steps we need to perform such as below in order to create the golden image so that it can be used in another platform 
    
    - download the patches 
    
    - install a package
    
    - pull down a script 
    
    - place files on the image 

  - these all steps `hashicorp packer` will going to eleminate and handle that for us in order to create the golden image
  
  - some of the `example of builder or providers` for the `hashicorp packer` is given down below 

    - AWS
    
    - Azure
    
    - Docker
    
    - Google Cloud
    
    - Openstack
    
    - VMWare
    
    - Digital Ocean


# Primary Usecase of Hashicorp Packer 

- `Create` `Golden Images` Across `Platforms(AWS/Azure/VMWare)` and `Environments`

- we can also want the `identical images` accross `multiple environments` such as `Dev/Test/PreProd/Prod`

- we want to make sure that `like for like environment` on which `new customized image going to run` 

<br/>

- `Packer` is super popular `While creating the image factory` , An `image factory` is based on the `new commits` and this goes along with `Continious Delivery`

- As the `Application changes` or `New Requirement identified for the New Application` , then we can `plug` the `New Requirement` into the `packer template`

- when we commit those `packer template configuration` to the repo , we can have a `CICD Job` that go ahead and `build the new image` from the `updated packer template configuration`

- we can have the `application deployment pipeline` can refer to the `latest golden image` that been `build` with `updated packer configuration` everytime

- it does not matter `no of times ` the `application need to deployed on the platform` , but `pipeline` always `grabs the latest golden image` thats been bbuild using the latest `updated packer configuration`

- we can `iterating over the application to add new feature` , we can pump the `new feature on to the packer template` and build a `golden image` from there which can be refer by the `Application on the platform`

<br/>

- `another way of the using the packer` is to `Automate Your Monthly Patching For New/Existing Workloads`

- when we `normally do` `patching` then we have to specify `downtime maintaince window` such as `saturday @ 2AM` , normally we uses `software to do that`

- for some of the `workload on old legecy application` we need to do the `handheld maintainance` 

- what we can do  with `hashicorp packer` is to have the `after the software update being released or pull all the latest software patches` , we can build `a new custom image with the updated software`

- which make sure we have the `fresh latest image` for our `application workload`

- a lot of time we need to make sure that `application workload` support something like `automatic patch update on the platform`

- maybe the `application` need some type of `manual hand helding` on installation so that `its not really prevelant to rebuild this thing every month for patches` , we have the `exception for automation`

- a lot of times `folks` want to use the `mutable infrastructure`, so that `placing all the application workload` with the `new image` or `application installation` thats `completely automated` , then updating the `monthly patching using hashicorp packer` will be super helpful

<br/>

- Create `Immutable Infrastructure` Using `Packer` in `CI/CD Pipeline`

- we can `stop fixing all the application workload` which are `running today` , stop `logging in` and `making changes` `whether thats updating application workload`

- we can actually use the `immutable infrastructure` just to `replace` the `whats go bad` with a `known good`

- if we have the `application workload` which is `completely automated` then `instead of fixing the broken application workload` we can `replace` that with `new image with application workload` with `known good`

- we can create `immutable infrastructure` using `packer` , we can build the `packer images` which is very specific and custom to the `application need`

# Benifits of Using Packer 

- `Hugh Benefit` for the `packer images` is that `your custom image` can be `version controlled`

- we have discuss the `packer implementation` using the `packer template`

- A `packer template` is a `place where we define the requirement for the packer build` 

- we can `commit` these `packer template containing the requirement for the packer build` into a `repo`

- by `commiting these changes` we can make sure the `packer images` `accross the board` is now `version controlled`

- `packer images` are `now being defined and versioned` just like `other deployment code in this area`

- rather than `manual control of image` such as 
  
  - we can `update` the `instance` after updating the `AMI` 
  
  - we have to shutdown the `already running instance running on preveious AMI` 
  
  - we need to go to the `automation stack` to `deploy the image with New AMI` `manually we don't have to do that `
  
- we can use `packer` `perform all those task together` , also version control the `packer images` and `application workload can use the latest packer image`

- we don't have maintain these `golen images` across multiple platform and updated in the platform 

<br/>

- another benefit of the `packer images` is that `consistent images` where we are running the `application workload` on the same `old configuration`

- when we `troubleshoot or deploy the application workload` then we know `exactly what should be there`

- we have the `like for like images` accross multiple `platforms and environment `

<br/>

- stop the `manual madness` and `automate everything` 

- `manually` have to `manage` across `multiple platform` which can be tiresome , which can be prone to `human error`

- if we are updating the `windows images` then after the update there can be second update which might be ignored if we are doing manual upgrade

- then their might be some workload which are `fully patched` and some are `suspectable to attack` 

- but if we are using something like packer we ensure all the images are being fully updated  

- `hashicorp packer` also reduces the `administrator overhead` for maintianing all the `images` accross `multiple platform`