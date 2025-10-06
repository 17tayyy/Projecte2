# 📗 Tasca 3 — Seguretat Lògica: recuperant accés a sistemes

Aquesta carpeta conté la documentació i les captures de la **Tasca 3** del **Projecte 2 — EverPia**.

---

## 📄 Contingut
- `solution.md` : documentació completa i procediment pas a pas  
- `img/` : captures de pantalla i proves (assegura't d'afegir imatges)  

➡️ [Accedir directament a la solució](./solution.md)

---

## 🧾 Breu descripció
Un portàtil amb **Zorin OS** (Linux) d’un directiu ha quedat bloquejat per oblit de contrasenya. El disc ha estat clònat i us han lliurat el disc virtual perquè hi treballeu sobre una màquina virtual per recuperar l’accés sense malmetre l’equip original.  
Un cop recuperat l’accés, el client vol que proposeu mesures per **fortificar l’accés al GRUB** i evitar que es pugui reiniciar la contrasenya amb el mateix procediment.

---

## 🎯 Objectius de la tasca
1. Accedir a la màquina virtual que conté el disc clònat.  
2. Explorar i identificar l’usuari existent al sistema.  
3. Recuperar o canviar la contrasenya d’aquest usuari i verificar l’accés.  
4. Investigar i aplicar mesures per **protegir GRUB amb contrasenya**.  
5. Documentar TOT el procediment amb captures i fonts.

---

## 🛠 Procediment (resum operatiu)
1. Crear una VM (VirtualBox/VMware) i adjuntar el disc virtual proporcionat.  
2. Arrencar la VM i entrar al menú GRUB (si el GRUB és accessible).  
3. Iniciar en mode recovery o editar la línia del kernel per obtenir shell root (`init=/bin/bash` o usar `single`), segons procediment.  
4. Muntar el sistema en escriptura si cal (`mount -o remount,rw /`).  
5. Llistar usuaris: `ls /home` i `cat /etc/passwd` per identificar l’usuari.  
6. Canviar la contrasenya: `passwd <usuari>` i comprovar login en l’entorn gràfic.  
7. Verificar accés i recuperar fitxers necessaris.  

> IMPORTANT: documenta cada pas i afegeix captures. No facis res sobre el disc original; treballa sempre sobre el disc clònat proporcionat.

---

## 🔐 Fortificació del GRUB (tasca d’investigació i aplicació)
- Investigar i documentar com activar protecció per contrasenya al GRUB (generar password hash amb `grub-mkpasswd-pbkdf2`, afegir `set superusers="nom"` i `password_pbkdf2 nom <hash>` al `/etc/grub.d/40_custom` o `/etc/grub.d/01_users`, regenerar config amb `update-grub`).  
- Configurar la VM perquè el GRUB estigui protegit i verificar que l’entrada d’edició de línia requereix contrasenya.  
- Aportar recomanacions addicionals (UEFI password, xifrat de disc LUKS, desactivar arrencada per USB si cal).

> **Cal incloure les fonts** d’on s’ha obtingut la informació i les comandes exactes utilitzades.

---

## ✅ Entregables
- `solution.md` amb:
  - Pas a pas dels passos realitzats (comandes i sortides rellevants).  
  - Captures de pantalla del procés.  
  - Llista d’usuaris trobats i comprovat canvi de contrasenya.  
  - Procediment i proves de protecció del GRUB.  
  - Fonts i enllaços utilitzats.  
- Carpeta `img/` amb les captures numerades.

---

## 📚 Material de suport / referències
- Disc virtual (proporcionat pel client)  
- Apunts **RA1AA4 — Seguretat Lògica**  
- Recuperant Password en Linux: https://waytoit.wordpress.com/2013/06/06/recuperando-password-en-ubuntu/  
(afegeix aquí altres fonts que facis servir i cita-les a `solution.md`)

---

## ⚠️ Consideracions ètiques i legals
Només treballar amb discos/clons proporcionats i autoritzats. Documentar permisos i autoritzacions del client. Qualsevol acció sobre equips reals ha d’estar autoritzada per escrit.

---

## 🏁 Objectiu final
Recuperar l’accés al sistema, protegir el procés d’arrencada contra atacs fàcils i lliurar un informe tècnic clar, reproduïble i justificat per al client.
