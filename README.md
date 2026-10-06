# dyn-dns.es Sync

App de Windows de [dyn-dns.es](https://dyn-dns.es), el DNS dinámico gratis hecho en España. Mantiene tus subdominios `tunombre.dyn-dns.es` apuntando a tu IP aunque tu operador la cambie.

- Inicias sesión una vez (usuario y contraseña, o Google).
- Eliges qué subdominios sincronizar, varios a la vez.
- Se queda en la bandeja del sistema y arranca con Windows.

## Descarga

Descarga `dyn-dns-sync-setup.exe` desde la [última versión](https://github.com/ChemaSanchez11/dyn-dns-sync/releases/latest).

El instalador todavía no está firmado digitalmente, así que Windows SmartScreen puede avisar al abrirlo: pulsa «Más información» y «Ejecutar de todas formas». Puedes comprobar que el fichero es el original con la huella SHA-256 que aparece en cada versión.

## Sin instalar nada

Si prefieres no instalar la app, desde una consola de administrador:

```
schtasks /create /tn "dyn-dns update" /tr "curl.exe -fsS https://dyn-dns.es/api/update?token=TU_TOKEN" /sc minute /mo 5
```

Más opciones (router, NAS, Raspberry Pi, Home Assistant) en las [guías](https://dyn-dns.es/guias).

## Contacto

[info@dyn-dns.es](mailto:info@dyn-dns.es) · [Estado del servicio](https://dyn-dns.es/estado)
