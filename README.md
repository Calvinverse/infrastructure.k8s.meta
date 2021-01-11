# infrastructure.k8s.meta

The kubernetes configuration files to create the meta environment


* Done via a Terraform or Helm script to deploy all the required services
* How are we going to deal with certificates and secrets etc.
* Bootstrap should work just from a repo, i.e. all you have done is `git clone`
  so the bootstrap script should be able to
  * Build the application, possibly into a docker container
  * Run the code(?)
  * Deploy the base infrastructure -> Meta environment
    * k8s cluster(?)
    * Consul masters
    * observability
    * storage
    * event system
    * api front-end
    * Service
  * Send data describing the environment that was just created
  * send commands to create the other environments that should be created(?)
* What do we do if there is no k8s cluster
  * microk8s
  * Azure k8s
