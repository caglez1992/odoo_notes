# ODOO GENERAL
#### SQL CONSTRAINTS
```python
_sql_constraints = [
    ('move_id_unique', 'UNIQUE(move_id)', 'La Factura debe ser un campo único'),
]
```


# ODOO 15

#### RETURN FORM VIEW
```python
view_id = self.env.ref('electronic_invoice.factura_electronica_form')
return {
    'name': 'Factura Electrónica',
    'type': 'ir.actions.act_window',
    'res_model': 'factura.electronica',
    'view_type': 'form',
    'view_mode': 'form',
    'views': [(view_id.id, 'form')],
    'target': 'current',
    'res_id': self.factura_electronica_id.id,
}
```
