# Box Vagrant usada no curso de Rails 5.x

Para usar essa box você precisa instalar o:

- VirtualBox
- Vagrant
- Git for Windows (para usuários Windows)

## Após a instalação dos itens acima, siga os passos abaixo, usando um terminal.

1- Instale o plugin do vagrant
```
vagrant plugin install vagrant-vbguest
```

2- Clone esse repositório
```
git clone https://github.com/jacksonpires/curso-rails
```

3- Inicie a box
```
vagrant up
```

4- Acesse o Cloud9 em **http://localhost:8181**  ou use o **vagrant ssh** para acessar a box via ssh.

## Dicas de comandos para gerir sua box

- Para pausar a box
```
vagrant suspend
```

- Para iniciar/levantar a box
```
vagrant up
```

- Para parar a box
```
vagrant halt
```