sa-jenkins-swarm-runner
=======================

[![Build Status](https://travis-ci.org/softasap/sa-jenkins-swarm-runner.svg?branch=master)](https://travis-ci.org/softasap/sa-jenkins-swarm-runner)


Basic role for jenkins runners based on swarm client plugin

Example of usage:

Simple

```YAML

     - {
         role: "sa-jenkins-swarm-runner",
         option_install_java: true,
         cd_address: https://cd.your.address,
         # specify user on your mothership jenkins
         cd_user: "{{ cd_env }}-builder",
         # specify user password on your mothership jenkins
         cd_pwd: ""

       }


```

Advanced

```YAML

     - {
         role: "sa-jenkins-swarm-runner",
         option_install_java: true,
         cd_address: https://cd.your.address,
         # specify user on your mothership jenkins
         cd_user: "{{ cd_env }}-builder",
         # specify user password on your mothership jenkins
         cd_pwd: "",
         agent_version: "3.15",
         agent_extra_params: "-disableClientsUniqueId -mode exclusive",
         cd_slave_executors: 1,
         agent_user: jenkins,
         agent_install_dir: /opt/jenkins,



       }


```



Usage with ansible galaxy workflow
----------------------------------

If you installed the `sa-jenkins-swarm-runner` role using the command


`
   ansible-galaxy install softasap.sa-nginx
`

the role will be available in the folder `library/softasap.sa-jenkins-swarm-runner`
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-jenkins-swarm-runner"
       }

```




Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Reach us:

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)

Discover other roles at  http://www.softasap.com/roles/registry_generated.html

visit our blog at http://www.softasap.com/blog/archive.html
