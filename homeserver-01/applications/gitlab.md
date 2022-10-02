
# GitLab #

Reconfigurar o gitlab

> `gitlab-ctl reconfigure

Editar o arquivo de configurações

> `nano /etc/gitlab/gitlab.rb`


## Problema ##
Caso não seja possível fazer push para o repositório remoto, executar este comando para desativar a necessidade de SSL Verification.

- ### Solução ###

    - > `git config --global http.sslVerify false`


## Problema ##
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories

- ### Solução ###
    - > `git pull origin master --allow-unrelated-histories`


## Problema ##
Remover um servidor remoto e adicionar outro.

- ### Solução ###
    - Primeiro liste os servidores remotos
    > `git remote -v`

    > `origin      git@gitlab.com:delftstack/programmingarticles.git (fetch)`
    > `origin      git@gitlab.com:delftstack/programmingarticles.git (push)`
    > `upstream    git@bitbucket.org:delftstack/test.git (fetch)`
    > `upstream    git@bitbucket.org:delftstack/test.git (push)`

    Escluindo o endereço desejado
    >`git remote rm upstream`