# Projecte: Recuperació i Fortificació d’Accés a un Sistema Linux (Zorin OS)

## Context

Després de la primera feina exitosa, la consultora rep un **encàrrec urgent** d’un **client** amb un problema de seguretat lògica:

> Un **portàtil amb Zorin OS** (basat en Linux) pertanyent a un **directiu** ha quedat **inaccessible** perquè s’ha **oblidat la contrasenya**.  
> El disc s’ha **clonat** a un **disc virtual** per treballar-hi de forma **segura**, sense risc per a l’equip original.

La tasca consisteix en:
1. **Recuperar l’accés** al sistema.
2. **Modificar la contrasenya** de l’usuari existent.
3. **Verificar l’accés correcte**.
4. **Proposar i implementar mesures** per **fortificar** el sistema, evitant que es pugui repetir aquest procediment fàcilment.

---

## Objectius

- Crear una **màquina virtual** amb el **disc virtual clonat** del client.  
- **Accedir al GRUB** i vulnerar el sistema per **resetar la contrasenya**.  
- **Identificar l’usuari** existent al sistema.  
- **Assignar una nova contrasenya** i comprovar que l’accés és possible.  
- **Investigar** com protegir el **GRUB** amb **contrasenya** per evitar vulneracions futures.  
- **Configurar** el sistema amb aquesta protecció.  
- **Documentar tot el procediment** amb imatges i fonts consultades.

---

## Recursos i materials

-  **Disc virtual** proporcionat pel client  
-  **Màquina virtual** creada amb VirtualBox o similar  
-  **Apunts:** RA1AA4 - *Seguretat Lògica*  
-  **Recurs de suport:** [Recuperant Password en Linux (WordPress)](https://waytoit.wordpress.com/2013/06/06/recuperando-password-en-ubuntu/)

---

## Tasques a realitzar

### 1. Creació de la màquina virtual
- Crear una màquina virtual i **connectar-hi el disc virtual** proporcionat.
- Verificar que arrenca correctament fins al menú del **GRUB**.

### 2. Vulneració de l’accés
- Entrar al **GRUB** i modificar els paràmetres d’arrencada per accedir com a **root**.
- Accedir al sistema en **mode de recuperació** o **single-user mode**.

### 3. Identificació de l’usuari
- Llistar usuaris del sistema amb:  
  ```bash
  cat /etc/passwd
