[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = GITCLUSTER.COM
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true

[realms]
 GITCLUSTER.COM = {
  kdc = clouderaseb00.gitcluster.com
  admin_server = clouderaseb00.gitcluster.com
 }

[domain_realm]
 .gitcluster.com = GITCLUSTER.COM
 gitcluster.com = GITCLUSTER.COM
