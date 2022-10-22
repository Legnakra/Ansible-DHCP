# Ansible-DHCP 
Servidor DHCP con Ansible (continuación de ([Escenario-Ansible-Vagrant](https://github.com/Legnakra/Escenario-Ansible-Vagrant))

![Escenario](/router.png)

## Preparación del escenario
El escenario que hicimos con Vagrant vamos a realizarlo a mano con máquinas virtuales en VirtManager con la misma configuración que la que teníamos en el escenario anterior. 
- Conectaríamos las máquinas a una red NAT sin dhcp (con IP estática) que utilizaríamos para configurar las máquinas por ansible. Esto soluciona el problema de que las direcciones IP cambien en vagrant y tengamos que cambiar el inventario cada vez que creemos el escenario.

## Configuración del playbook
1. La máquina cliente de la práctica anterior, que tiene instalado el servidor web, debe tener la misma IP que la que le asígnate estáticamente, por lo tanto haremos una reserva para que tenga la misma IP.
2. Al añadir una nueva máquina a la red local (recuerda que no se le instalará el servidor web) se configurará de forma dinámica.
3. Crea un nuevo rol en el playbook de ansible llamado dhcp que configure el servidor DHCP de forma correcta. Quizás sea necesario modificar el comportamiento de algún rol de la práctica anterior.
4. Todos los parámetros que reparta el servidor DHCP, así como cualquier otro dato, por ejemplo la dirección MAC del cliente se guardarán en variables.
5. Añade una nueva máquina al escenario conectada a la red interna muy aislada. Vuelve a ejecutar el playbook y comprueba que todo funciona de forma correcta.

## Autora :computer:
* María Jesús Alloza Rodríguez
* :school:I.E.S. Gonzalo Nazareno :round_pushpin:(Dos Hermanas, Sevilla).