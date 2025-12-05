Apartado 1  

<img width="1329" height="889" alt="image" src="https://github.com/user-attachments/assets/43f2f6e7-da0a-4856-b2b7-259880052537" />
<img width="1401" height="958" alt="Captura de pantalla 2025-12-04 205750" src="https://github.com/user-attachments/assets/6b2786f4-ddc8-41b1-875a-9d1f58f782fd" />
<img width="1645" height="942" alt="image" src="https://github.com/user-attachments/assets/c333d2d7-f054-433f-8b82-e17826cb4133" />


Apartado 2  

<img width="1294" height="965" alt="image" src="https://github.com/user-attachments/assets/0eba2b0e-7750-4114-9e09-1baee029c387" />
<img width="1239" height="919" alt="image" src="https://github.com/user-attachments/assets/e727fb18-345c-47ba-bfde-0b776ecdbfc8" />

Apartado 3  
<img width="1073" height="597" alt="image" src="https://github.com/user-attachments/assets/41ff8a3a-020d-469c-bb73-0995e2bfd975" />

Apartado 4 

<img width="1467" height="896" alt="image" src="https://github.com/user-attachments/assets/39422db2-0ce9-406f-b9e6-07cb870581e5" />
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
