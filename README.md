## DESCRIPCION


Este repositorio recogerá diversos roles sueltos para realizar pruebas y para probar diversos modulos



Playbook de Ansible

Este es un playbook de Ansible diseñado para automatizar tareas de configuración y gestión de sistemas. Utiliza Ansible, una herramienta de automatización de TI de código abierto, para simplificar la implementación y la gestión de la infraestructura.
Requisitos previos

Asegúrese de tener los siguientes requisitos previos antes de ejecutar este playbook:

    Ansible instalado en el sistema de control.
    Acceso SSH a los nodos de destino.
    Inventario de hosts configurado en el archivo inventory.ini.

Estructura del Proyecto

css

.
├── playbook.yml
├── inventory.ini
├── roles/
│   ├── common/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   └── defaults/
│   │       └── main.yml
│   └── webserver/
│       ├── tasks/
│       │   └── main.yml
│       └── defaults/
│           └── main.yml
└── README.md

Ejecución del Playbook

Ejecute el playbook utilizando el siguiente comando:

bash

ansible-playbook -i inventory.ini playbook.yml

Asegúrese de ajustar el archivo de inventario según sus nodos de destino y configuraciones específicas.
Roles
common

Este rol se encarga de realizar configuraciones comunes en todos los nodos. Puede personalizar las tareas en roles/common/tasks/main.yml según sus necesidades.

Variables predeterminadas: roles/common/defaults/main.yml
webserver

Este rol instala y configura un servidor web. Puede personalizar las tareas en roles/webserver/tasks/main.yml y ajustar las variables predeterminadas en roles/webserver/defaults/main.yml.
Contribuciones

Si desea contribuir, abra un problema o envíe una solicitud de extracción. ¡Estamos abiertos a mejoras y nuevas ideas!
Licencia

Este playbook de Ansible está bajo la licencia MIT.
