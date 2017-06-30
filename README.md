This repository is the home to patches created against Peopletools Puppet
modules to correct issues found in our environment.

# File list
    ./README.md

## pt_profile
    ./pt_profile/manifests/pt_system/users.pp.patch

## pt_config
    ./pt_config/lib/puppet/provider/pt_des_domain/des_domain.rb.patch
    ./pt_config/lib/puppet/provider/webappdomain.rb.patch
    ./pt_config/lib/puppet/type/pt_des_domain.rb.patch

## pt_setup
    ./pt_setup/templates/linux_user_environment.erb.patch

## pt_deploy
    ./pt_deploy/lib/puppet/provider/pt_deploy_apphome/deploy_apphome.rb.patch
    ./pt_deploy/lib/puppet/provider/pt_deploy_tuxedo/deploy_tuxedo.rb.patch
    ./pt_deploy/lib/puppet/provider/pt_deploy_weblogic/deploy_weblogic.rb.patch
