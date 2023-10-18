# ODOO GENERAL
#### OPTIONS
```xm;
options="{'no_open': True, 'no_create_edit': True, 'no_create': True, 'no_quick_create':True}"
```

#### SQL CONSTRAINTS
```python
_sql_constraints = [
    ('move_id_unique', 'UNIQUE(move_id)', 'La Factura debe ser un campo único'),
]
```


# RETURN FORM VIEW (MODAL)

#### ODOO 9
```python
form_view_id = self.env.ref('oe_oferta.oe_cargo_docente_acta_form')
return {
    'name': 'Agregar Docente',
    'type': 'ir.actions.act_window',
    'view_type': 'form',
    'view_mode': 'form',
    'views': [(form_view_id.id, 'form')],
    'view_id': form_view_id.id,
    'res_model': 'oe.cargo.docente',
    'target': 'new',
    'context': context
}
```

#### ODOO 15
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
