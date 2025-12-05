## SXE TAREA 14

### Apartado 1  
Una vez de conectar pgAdmin con Odoo con la `demo`...  

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/43f2f6e7-da0a-4856-b2b7-259880052537" />

Creamos en en apartado de 'tablas', una tabla con los campos mostrados a continuación...  

<img width="700" height="500" alt="Captura de pantalla 2025-12-04 205750" src="https://github.com/user-attachments/assets/6b2786f4-ddc8-41b1-875a-9d1f58f782fd" />
<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/c333d2d7-f054-433f-8b82-e17826cb4133" />  

### Apartado 2   
Insertamos 5 registros inventados en la tabla a través de una sentencia SQL.  

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/0eba2b0e-7750-4114-9e09-1baee029c387" />  
<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/e727fb18-345c-47ba-bfde-0b776ecdbfc8" />  

### Apartado 3  
Realiza una consulta donde se muestren todos los datos de la tabla EmpresasFCT 
ordenados por fechaContacto, de modo que en la primera fila salga el que tenga la 
fecha más reciente. 

Mediante los comandos `SELECT * FROM public."EmpresasFCT" ORDER BY "fechaContacto" DESC;` , nos generará lo pedido. 

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/41ff8a3a-020d-469c-bb73-0995e2bfd975" />  

### Apartado 4
Realiza una consulta que permita obtener un listado de todos los contactos de Odoo (no empresas) con la siguiente información: 
- Nombre
- Cuya ciudad NO sea Tracy
- Nombre comercial de la empresa ordenados alfabéticamente por el nombre comercial de la empresa.

`SELECT name, commercial_company_name FROM public.res_partner where is_company=FALSE and city!='Tracy' ORDER BY commercial_company_name`  

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/ca54ba67-64c3-4f7f-8e5f-9c30a4cdaf21" />

APARTADO 5  

<img width="1599" height="876" alt="image" src="https://github.com/user-attachments/assets/cb6ab1dd-e48a-46b2-b07d-2941443ce4ed" />  
select invoice_partner_display_name,name, invoice_date, amount_untaxed FROM public.account_move where move_type='out_refund' and invoice_date is not null order by invoice_date DESC;

APARTADO 6  
select invoice_partner_display_name nome_empresa, count(*) num_facturas, SUM(amount_untaxed) suma_total_facturas
FROM public.account_move 
WHERE move_type='out_invoice' and state='posted'
GROUP BY nome_empresa having count(*)>2
;  

<img width="1635" height="1019" alt="image" src="https://github.com/user-attachments/assets/6aebaebb-60de-4f6f-9246-33e7a332cdb0" />

APARTADO 7    
UPDATE public.res_partner
	SET  email=REPLACE(email,'%@bilbao.example.com','bilbao.bizkaia.eus') WHERE email LIKE '%@bilbao.example.com';  
<img width="1692" height="995" alt="image" src="https://github.com/user-attachments/assets/8d7a2db0-e44c-4822-a1f9-e3a220b2d34a" />  




