# Repositorio local vs remoto

Un **repositorio local** es el repositorio Git que está almacenado en tu propio ordenador. Ahí es donde trabajas, haces cambios y creas commits.

Por ejemplo:

```
PC
└── MiProyecto/
    ├── src/
    ├── pom.xml
    └── .git/
```

Un **repositorio remoto** es otro repositorio que está almacenado en un servidor y al que puedes conectarte desde tu ordenador. GitHub es un ejemplo de servicio que aloja repositorios remotos.

```
Tu PC                         GitHub
  │                              │
  └── MiProyecto                 └── MiProyecto
      └── .git                       └── repositorio remoto
```

Los dos repositorios pueden contener el mismo proyecto, pero **son repositorios independientes**. Los cambios que haces en tu repositorio local no aparecen automáticamente en el remoto.

Más adelante utilizaremos comandos para sincronizarlos:

```
Local  ── push ──→  Remoto
Local  ←─ pull ───  Remoto
```

También puedes tener un repositorio local aunque no exista ningún repositorio remoto. Por ejemplo, puedes usar Git completamente de forma local sin utilizar GitHub.