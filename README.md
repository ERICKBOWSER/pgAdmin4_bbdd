
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

```
INSERT INTO public.ingredientes (
codIngredientes, nombreIngrediente, codMacronutrientes)
VALUES (1, 'pollo', 1),
	   (2, 'arroz', 2),
	   (3, 'pimiento', 2),
	   (4, 'manzana', 2),
	   (5, 'aceite de oliva virgen extra', 3),
	   (6, 'merluza', 1),
	   (7, 'tofu', 1),
	   (8, 'quinoa', 2);
```

```
INSERT INTO public.Macronutrientes(
codMacro, nombre)
VALUES(1, 'Proteinas'),
	(2, 'Carbohidratos'),
	(3, 'Grasas');
```

```
INSERT INTO public.recetas(
codReceta, nombreReceta, elaboracion, codCliente)
VALUES(1, 'Ensalada de quinoa y pollo','sdfnhksdañklfja', 1),
	(2, 'Salteado de verduras y tofu','sdfnhksdañklfja', 2),
	(3, 'Arroz con pollo','sdfnhksdañklfja', 3),
	(4, 'Tarta de manzana','sdfnhksdañklfja', 4),
	(5, 'Gazpacho andaluz','sdfnhksdañklfja', 5),
	(6, 'Lasaña de carne','sdfnhksdañklfja', 6),
	(7, 'Pisto','sdfnhksdañklfja', 7),
	(8, 'Crema de calabaza','sdfnhksdañklfja', 8);
```

```
INSERT INTO public.listaIngredientes(
codReceta, codIngredientes, cantidad)
VALUES (1, 3, 200), (1, 6, 100), (1, 7, 150),
	(2, 2, 300), (2, 3, 200), (2, 5, 50),
       (3, 2, 150), (3, 6, 100), (3, 7, 200),
       (4, 4, 250), (4, 8, 150), (4, 2, 100),
       (5, 3, 200), (5, 4, 100), (5, 5, 50),
       (6, 1, 200), (6, 6, 150), (6, 2, 100),
       (7, 3, 300), (7, 1, 150), (7, 7, 200),
       (8, 8, 250), (8, 2, 150), (8, 4, 100);

```

```
SELECT * FROM public.clientes;
```

```
UPDATE public.recetas
	SET elaboracion = "prueba"
	WHERE idReceta = 1;
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














