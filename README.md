This repository is the home to patches created against Peopletools Puppet
modules to correct issues found in our environment.

These are all built against the 8.56 delivered modules. Likely they will
not 'git apply' against the 8.55 modules due to additions from Oracle, but
they are all simple to replicate with copy/paste.

# File list
    ./README.md

## pt_profile
users.pp is patched to remove the 'chage' command run against psadm2.
We set a real password and do not want this user blocked from any work. In 
particular this will break setting up cron jobs as psadm2.

    ./pt_profile/manifests/pt_system/users.pp.patch

## pt_config
Everything in here is for the CRM Online Marketing DES server setup. If you do
not use CRM Online Marketing you likely will not need any of this.

    ./pt_config/lib/puppet/provider/pt_des_domain/des_domain.rb.patch
    ./pt_config/lib/puppet/provider/webappdomain.rb.patch
    ./pt_config/lib/puppet/type/pt_des_domain.rb.patch

## pt_setup
Currently this only sets the TUXDIR back to the 8.55 version number. If you are
using the 8.55 modules this won't apply to you. I will update this to templatize
that version so that 8.56 and 8.55 can coexist in the puppet codebase.

    ./pt_setup/templates/linux_user_environment.erb.patch

## pt_deploy
These correct minor typos and add functionality for patching middleware during 
the Puppet deploys.

    ./pt_deploy/lib/puppet/provider/pt_deploy_apphome/deploy_apphome.rb.patch
    ./pt_deploy/lib/puppet/provider/pt_deploy_tuxedo/deploy_tuxedo.rb.patch
    ./pt_deploy/lib/puppet/provider/pt_deploy_weblogic/deploy_weblogic.rb.patch
