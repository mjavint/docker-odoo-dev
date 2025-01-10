# VSCode + Docker para el desarrollo en Odoo con completado inteligente

1. Instalar VSCode de su página oficial - <https://code.visualstudio.com>
2. Instalar extensiones en vscode para la productividad:

   - Odoo IDE
     <https://marketplace.visualstudio.com/items?itemName=trinhanhngoc.vscode-odoo>
   - Odoo Shortcuts
     <https://marketplace.visualstudio.com/items?itemName=mvintg.odoo-file>
   - Owl Vision <https://marketplace.visualstudio.com/items?itemName=Odoo.owl-vision>

3. Crear el espacio de trabajo importando el código fuente de Odoo
4. Configurar y modificar el fichero pyrightconfig.json
5. Compilar la imagen de docker con el fichero Dockerfile
6. Configurar las variables en el .env
7. Configurar el debug en vscode

Ejemplo:

```json
{
  "name": "Docker Odoo Attach",
  "type": "debugpy",
  "request": "attach",
  "connect": {
    "host": "0.0.0.0",
    "port": 8888
  },
  "pathMappings": [
    {
      "localRoot": "${workspaceFolder}/addons",
      "remoteRoot": "/var/lib/odoo/custom_addons"
    },
    {
      "localRoot": "<Path Odoo Server>/addons",
      "remoteRoot": "/var/lib/odoo/odoo/addons"
    }
  ]
}
```
