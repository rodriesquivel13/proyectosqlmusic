# Base de datos en música


Hemos realizado una estructura de base de datos para organizar su música de manera eficiente. A continuación, le presentamos una descripción detallada de la estructura, las relaciones entre las tablas y una explicación del modelo entidad-relación utilizado.

- Tabla "recordlabel":

Esta tabla almacena información sobre las compañías discográficas.
Tiene dos columnas principales: LabelId y Name.
La columna LabelId se establece como llave primaria, lo que garantiza su unicidad en cada registro.

-Tabla "artist":

Esta tabla contiene información sobre los artistas musicales.
Tiene tres columnas principales: LabelId, ArtistId y Name.
La columna ArtistId se define como llave primaria, asegurando su unicidad.
La columna LabelId se establece como llave foránea, lo que significa que está relacionada con la tabla "recordlabel".
Esto permite establecer una conexión entre un artista y la compañía discográfica a la que pertenece.

-Tabla "album":

Esta tabla almacena detalles de los álbumes musicales.
Tiene cuatro columnas principales: ArtistId, AlbumId, Name y Year.
La columna AlbumId se designa como llave primaria, asegurando su unicidad.
La columna ArtistId se establece como llave foránea, lo que indica la relación con la tabla "artist".
Esta relación permite vincular un álbum a un artista específico.

-Tabla "song":

Esta tabla registra información sobre las canciones.
Tiene cuatro columnas principales: AlbumId, SongId, Name y Duration.
La columna SongId se define como llave primaria, garantizando su unicidad.
La columna AlbumId se establece como llave foránea, creando una relación con la tabla "album".
Esto permite asociar una canción a un álbum en particular.
El modelo entidad-relación utilizado en esta estructura de base de datos se compone de las siguientes entidades y sus relaciones:

Entidad "RecordLabel": Representa una compañía discográfica y tiene una relación de uno a muchos con la entidad "Artist". Una compañía discográfica puede tener varios artistas, pero un artista solo pertenece a una compañía discográfica.

Entidad "Artist": Representa un artista musical y tiene una relación de uno a muchos con la entidad "Album". Un artista puede tener varios álbumes, pero un álbum pertenece a un único artista.

Entidad "Album": Representa un álbum musical y tiene una relación de uno a muchos con la entidad "Song". Un álbum puede tener varias canciones, pero una canción pertenece a un único álbum.

Entidad "Song": Representa una canción y está relacionada con la entidad "Album" mediante una relación de uno a muchos. Una canción pertenece a un único álbum, pero un álbum puede tener varias canciones.

Este modelo entidad-relación permite representar las relaciones entre las entidades de manera clara y facilita la comprensión de la estructura de la base de datos.

