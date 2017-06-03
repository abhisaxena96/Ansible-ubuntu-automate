##Ansible

## Tag's

- [Fe-www] (#fe-www)
- [Redis](#redis)
- [Postgresql] (#postgresql)
- [Jenkins] (#jenkins)
- [Graylog] (#graylog)
- [Elasticsearch] (#elasticsearch)
- [Testrail] (#testrail)

## Fe-WWW
```
 - deploy-fe             :
 - deploy-all            :
 - deploy-www            :
 - config-www            :
 - config-all            :
 - config-fe             :
 - config-custom         :
 - config-sysctl         :
 - nginx-reload-fe       :
 - nginx-reload-www      :
 - nginx-reload-all      :
 - nginx-reload          :
 - sitemap               :
 - sitemap-www           :
 - sitemap-fe            :
 - sitemap-all           :
 - pm2-www               :
 - pm2-fe                :
 - pm2-all               :
 - pm2                   :
 - pm2-www-reload        :
 - pm2-reload            :
 - pm2-start             :
 - pm2-display           :
 - pm2-www-display       :
 - pm2-check             :
 - pm2-www-check         :
 - pm2-www-transfer      :
 - pm2-transfer          :
 - permission-pm2        :
 - permission-www        :
 - permission-all        :
 - permission-fe         :
 - symlink-www           :
 - symlink-fe            :
 - symlink-all           :
 - symlink               :
 - maxmind-fe            :
 - maxmind-www           :
 - maxmind-all           :
 - maxmind               :
 - npm-update            :
 - npm-update-fe         :
 - npm-update-www        :
 - npm-update-all        :
 - npm                   :
 - prune-npm-fe          :
 - prune-npm-www         :
 - prune-npm-all         :
 - prune-npm             :
 - env                   :
 - env-www               :
 - env-fe                :
 - env-all               :
 - packages              :
 - nodejs-packages       :
 - npm-packages          :
 - remove-www            :
 - remove-all            :
 - remove-fe             :
 - clone-www             :
 - clone-all             :
 - clone-fe              :
```

## Redis
```
 -redis        : Deploy Full Redis Stack
 -redis-mount  : Mount storage
 -redis-6380   : Deploy Redis for 6380 Port only
 -redis-6381   : Deploy Redis for 6381 Port only
 -redis-config : Copy Redis conf for both 6380/6381
 -mount        : Mount storage
```

## Postresql
```
 -psql               : Deploy full postresql
 -bi-psql-install    : Deploy full postresql
 -bi-psql            : Deploy full postresql
 -bi-psql-mount      : Mount storate
 -bi-psql-config     : Copy Postresql config/host-bases authenticaiton
 -bi-psql-auth       : Copy Postresql host-bases authenticaiton
 -mount              : Mount storage
```
## Jenkins
```
 - jenkins
 - jenkins-plugins
 - plugins
 - jenkins-ssl
 - ssl
 - no-ssl
 - jenkins-no-ssl
 - start
 - jenkins-start
 - keys
 - jenkins-keys
 - pkg
 - jenkins-pkg
```
## Graylog
```
 - graylog                    : Deploy Graylog
 - remove-deb                 : Remove .deb file after setup is done
 - remove-override            : Remvoe override file
 - graylog-remove-override    : Remvoe override file
 - graylog-log4j2-conf        : Copy log4j2.conf
 - conf                       : Copy log4j2.conf & graylog.conf
 - graylog-conf               : Copy graylog.conf
 - graylog-apt                : Apt-get install graylog
 - graylog-folder             : Create data folder
 - nginx                      : Install nginx
 - nginx-conf                 : Copy nginx conf
 - graylog-nginx              : Install nginx
 - graylog-conf               : Copy nginx conf
```

## Elasticsearch
```
 - plugins                    : Install Plugins
 - elasticsearch              : Install Full elasticsearch
 - elasticsearch-plugins      : Install Plugins
 - elasticsearch-start        : start elasticsearch service
 - elasticsearch-conf         : Copy Conf
```

# Testrail
```
 - testrail              : Deploy Testrail
 - testrail-deploy       : Deploy Testrail
 - deploy                : Deploy Testrail
 - deploy-live           : Deploy Testrail
 - deploy-master         : Deploy Testrail
 - git-clone             : Clone Repo
 - live-repo             : Clone Repo
 - sendmail              : Install Sendmail
 - testrail-php          : Install ioncube 5.6 && Add ioncube in cli/php.ini && add ioncube in fpm/php.ini
 - testrail-ioncube      : Install ioncube 5.6 && Add ioncube in cli/php.ini && add ioncube in fpm/php.ini
 - app-config            : Copy .env
 - varfolder             : Misc folder exist and writable
 - reset-permissions     : Misc folder exist and writable && chown www
 - tf                    : Create testrail cron
 - travelfusion          : Create testrail cron
 - queue                 : Create testrail cron
 - pnr                   : Create testrail cron
 - cronjobs              : Create testrail cron
 - link-folder           : Symlink release to website folder
 - symlink               : Symlink release to website folder
 - permissions           : Chown www
 - reload-nginx          : Reload nginx
 - reload-php-fpm        : Reload php-fpm
 - nginx-version         : Check nginx version
 - nginx                 : Install nginx
 - nginx-install         : Install nginx
 - nginx-reload          : Nginx reload
 - nginx-config          : Copy nginx conf
 - site.d                : Copy nginx conf
 - nginx-ssl             : Transfer SSL
 - sites-enabled          : Transfer sites-enabled nginx conf
```

