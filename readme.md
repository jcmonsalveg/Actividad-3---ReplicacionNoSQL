# REPLICAS EN MONGODB

La replicación es la acción de sincronizar la información de una base de datos a través de múltiples servidores, de tal manera que se pueda garantizar la redundancia y la disponibilidad de los datos. 

En el conjunto de réplicas existen varios nodos, de los cuales hay uno primario o master y varios esclavos o secundarios. Dentro del conjunto de nodos se puede tener un árbitro, este es un nodo que participa en las elecciones para la elección del nodo primario frente a una posible caída del nodo primario. la configuración mínima de un réplica set pide, entonces, un nodo primario y dos secundarios. 

Entre los nodos creados existe una comunicación constante en la cual se verifica la existencia de los mismos (heartbeat). Frente a una caída de un servidor (donde reposa uno de los nodos), los demás nodos garantizan que no exista pérdida de la información, por ejemplo si se cae el nodo primario sucede una elección entre los nodos existentes y uno de los que quedan vivos asume el nodo de primario. Cuando el nodo caído se levante, se levantará como nodo secundario, ocurre una resincronización y se estabilizará el servicio. 

# REQUERIMIENTOS NO FUNCIONALES

•	La base de datos debe permitir realizar todas las operaciones de consulta necesarias.
•	La base de datos debe estar disponible 24/7
•	Se debe garantizar la seguridad de la información.
•	Debe permitir el acceso de varios usuarios al mismo tiempo (concurrencia)
•	Se debe garantizar la fiabilidad de la información. 
•	Debe permitir la escalabilidad horizontal para el crecimiento del negocio.


