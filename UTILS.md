# Útiles

## Master Password

`88mr-i2sy-jenm`

## Master Password Encriptada

`$pbkdf2-sha512$25000$oZSylpJyzrn33vs/53xPiQ$10slfAFf/Z2fnDRjlTGr9Tp0oZoKxDd9yDP1WgbiONGeXOHxLur7zG21b83PDwEDUFEXLDdPAczuzx3PAGMsvg`

## Establecer y restablecer la password del usuario administrador de Odoo

```sql
UPDATE res_users SET PASSWORD = '$pbkdf2-sha512$25000$oZSylpJyzrn33vs/53xPiQ$10slfAFf/Z2fnDRjlTGr9Tp0oZoKxDd9yDP1WgbiONGeXOHxLur7zG21b83PDwEDUFEXLDdPAczuzx3PAGMsvg' WHERE id = 2;
```

## Usuario Admin de Odoo

```sql
SELECT login, PASSWORD FROM res_users WHERE id = 2;
```

### Actualizar la fecha de creación y expiración de la base de datos Enterprise

```sql
UPDATE ir_config_parameter SET value = to_char(CURRENT_TIMESTAMP, 'YYYY-MM-DD HH:MI:SS') WHERE key = 'database.create_date';
UPDATE ir_config_parameter SET value = to_char(CURRENT_TIMESTAMP + INTERVAL '30 days', 'YYYY-MM-DD') WHERE key = 'database.expiration_date';
```
