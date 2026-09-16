# Git vs GitHub

**Git y GitHub son cosas diferentes**, aunque trabajan juntos.

**Git** es el sistema de control de versiones que se ejecuta en tu ordenador. Se encarga de registrar los cambios de tus proyectos mediante commits, ramas, historial, etc.

**GitHub** es una plataforma online que permite alojar repositorios Git en servidores y trabajar con ellos desde Internet.

Por ejemplo, puedes tener:

```
Tu ordenador
└── MiProyecto
    └── .git
```

Ese es tu **repositorio local**, gestionado por Git.

Y en GitHub puedes tener una copia del repositorio:

```
GitHub
└── MiProyecto
```

Ese será el **repositorio remoto**.

Git puede funcionar perfectamente **sin GitHub**. Puedes crear commits, ramas, consultar el historial y recuperar cambios aunque nunca subas el proyecto a Internet.

GitHub, en cambio, utiliza Git como base para ofrecer funciones como repositorios remotos, Pull Requests, colaboración, Code Review e Issues.

La relación básica es:

```
Git
↓
Controla las versiones de tu proyecto

GitHub
↓
Aloja repositorios Git y facilita compartirlos y colaborar
```