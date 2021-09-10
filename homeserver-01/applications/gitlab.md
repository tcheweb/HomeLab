

Caso não seja possível fazer push para o repositório remoto, executar este comando para desativar a necessidade de SSL Verification.

> `git config --global http.sslVerify false`

Reconfigurar o gitlab

> `gitlab-ctl reconfigure

Editar o arquivo de configurações

> `nano /etc/gitlab/gitlab.rb`


 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories

> `git pull origin master --allow-unrelated-histories`