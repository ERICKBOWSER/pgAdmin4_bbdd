
Crear servidor:

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/3dba4809-3325-473e-8317-6db65ff5b16c"> </p>


General:
* Name: es el nombre que va a tener el servidor
* Server Group: el grupo al que va a pertenecer

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/0688a7f6-2ef4-4925-aa38-8d4bb48b97a9"> </p>

Connection: 

* Host name: url de la bbdd
* Port: puerto al que se va a conectar
* Username: usuario con acceso
* Password: contraseña

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/3e5e71ad-cf11-4fa9-b2ba-13766823ddac"> </p>


Mostrar los datos de una tabla:

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/62b9c50f-77a1-4173-b4a4-970e9a4b7e70"> </p>

IMPORTANTE: no hacer si hay muchos datos en la bbdd el "All Rows" ya que puede tumbar la conexión dependiendo la cantidad.

Crear tabla: 

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/0329abd0-5441-4939-ad45-b7639438b6bc"> </p>

Solo cambiamos el Name que es el nombre que va a tener la tabla, el resto por defecto.

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/ecbc2d12-1cb1-4281-a82f-dfc82afef7a0"> </p>

Columnas que va a tener

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/18791a0d-5ab7-47a0-ada0-bb828f66c52d"> </p>

Query tool, para que se habrá una consola para poder añadir los datos manualmente

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/696d043b-c33b-4bb1-b292-a9abe16aaf0f"> </p>

Unique para el email:

```
ALTER TABLE public.clientes
ADD CONSTRAINT UQ_email Unique(email)
```



Insertar datos:

```
INSERT INTO public.clientes(
codcliente, nombre, apellido1, apellido2, email)
VALUES(1, 'Juan', 'Pérez', 'Gómez', 'juanperez@mail.com'),
	(2, 'María', 'González', 'Fernández', 'mariagonzalez@mail.com'),
    (3, 'Pedro', 'Sánchez', 'Jiménez', 'pedrosanchez@mail.com'),
    (4, 'Ana', 'Martínez', 'Ruiz', 'anamartinez@mail.com'),
    (5, 'Miguel', 'Hernández', 'Pérez', 'miguelhernandez@mail.com'),
     (6, 'Sofía', 'López', 'Santos', 'sofialopez@mail.com'),
      (7, 'David', 'García', 'Martín', 'davidgarcia@mail.com'),
      (8, 'Elena', 'Rodríguez', 'Vázquez', 'elenarodriguez@mail.com');
```

Eliminar datos:

```
DELETE FROM public.clientes 
WHERE id = 2;
```

Crear columna:

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/df6c919f-74bb-4b9f-9093-c7e4a42171ee"> </p>

Definition:

* Data type: se elige el tipo de dato que va a almacenar
* IMPORTANTE: los string se guardan como character varying

<p align="center"> <img src="https://github.com/ERICKBOWSER/pgAdmin4_bbdd/assets/92431188/1be99fc7-7cb1-4c23-99a9-32d8f198c009"> </p>














