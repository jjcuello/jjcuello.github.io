## Bienvenidos a mi página!

Está página web en github es una pequeña parte del proceso de aprendizaje para uno de mis hobby de toda mi vida: la informática. Gracias a mi mentor en el área: @gomix he ido aprendiendo de a poco temas de software libre, servidores y más.

Los invitó a pasearse por estás breves lineas y compartir.

### Código

El objetivo primordial es compartir las pequeñas experienzas con los diferentes códigos para ayudar a que otros tambíen aprendan:

```Código
# Ejemplo de my primer playbook en ansible

---
- name: instalar openvpn 
  hosts: virtual
  user: jcuello
  become: yes
  become_method: su
  tasks:
    - name: install epel-release
      yum: name=epel-release state=latest
    - name: upgrade all packages
      yum: name=* state=latest
    - name: install openvpn
      yum: name=openvpn state=latest
    - name: download easyrsa 
      get_url:
        url: https://github.com/OpenVPN/easy-rsa-old/archive/2.3.3.tar.gz
        dest: /tmp/easyrsa
    - name: create directory
      file:
        path: /etc/openvpn/easy-rsa
        state: directory
    - name: extract easyrsa
      unarchive:
        src: /tmp/easyrsa
        dest: /etc/openvpn/easy-rsa
        remote_src: yes
```

Para más detalles de cómo podemos adentrarnos en esté fascinante mundo te recomiendo visitar: http://redmine.cautivatech.com/redmine/projects/knowledge-base/wiki/Knowledge_Base_Wiki

Ajedrez

No podría dejar pasar por alto mi gran pasión y la disciplina a la cual le dedico mi vida profesional. Los invitó a solucionar el problema del día:

<script src="https://lichess.org/training/embed?theme=auto&bg=auto"></script>

Información de contácto:

jcuello@anaj.org.ve
