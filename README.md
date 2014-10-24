puppet-consul_template
======================

Initial version of a puppet-consul_template module.

Will install, and configure consul_template.

Tested on EL6

Init script generated by jordansissel/pleaserun

Requires puppetlabs-concat

Usage: 
      
      include consul_template
      consul_template::template {'nginx':
          source      => '/etc/consul-template/nginx.conf.ctmpl',
          destination => '/tmp/nginx-snippet.conf',
          command     => '/etc/init.d/nginx restart',
      }


Do note that putting the ctmpl file in place place is outside of this module scope.
It can e.g. be done in the profile.


