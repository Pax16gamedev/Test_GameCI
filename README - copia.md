# Guía para Pull Requests

## Convención de nombres de ramas
Para mantener la consistencia y facilitar la gestión del código, todas las ramas deben seguir esta convención de nombres:

- **`feature/<nombre>`**: Para implementar nuevas características o funcionalidades.
  - Ejemplo: `feature/add-new-character`
- **`bugfix/<nombre>`**: Para corregir errores detectados.
  - Ejemplo: `bugfix/fix-character-animation`
- **`hotfix/<nombre>`**: Para resolver problemas críticos en producción.
  - Ejemplo: `hotfix/fix-game-crash`
- **`fix/<nombre>`**: Para corregir problemas en desarrollo.
  - Ejemplo: `fix/player-movement`
- **`enhancement/<nombre>`**: Para mejoras en funcionalidades existentes.
  - Ejemplo: `enhancement/improve-ai-logic`
- **`refactor/<nombre>`**: Para reorganizar o limpiar código sin cambiar su funcionalidad.
  - Ejemplo: `refactor/reorganize-level-scripts`
- **`documentation/<nombre>`**: Para cambios o adiciones a la documentación.
  - Ejemplo: `documentation/add-setup-guide`

### **Reglas adicionales**
- Usa nombres descriptivos para las ramas.
- Evita caracteres especiales o espacios en los nombres de las ramas.

---

## Proceso para crear un Pull Request (PR)

### **1. Crear una rama nueva**
Asegúrate de crear la rama desde la rama correspondiente:
- **`DESARROLLO`**: Para nuevas características y correcciones generales.
- **`PRE`**: Solo para preparar cambios antes de pasar a producción.

#### **Ejemplo de creación de rama:**
```bash
git checkout DESARROLLO
git pull origin DESARROLLO
git checkout -b feature/add-new-character
```

### **2. Realizar los cambios y commit**
Realiza los cambios necesarios y asegúrate de que los commits sean claros y concisos. 

#### **Convención de mensajes de commit:**
- Describe qué se hizo en el commit.

Ejemplo:
```bash
git commit -m "Add new character selection screen"
```

### **3. Subir la rama al repositorio**
Sube tu rama al repositorio remoto.

```bash
git push origin feature/add-new-character
```

### **4. Crear el Pull Request**
1. Ve a la página del repositorio en GitHub.
2. Haz clic en **"Pull requests"**.
3. Selecciona la rama base (por ejemplo, `DESARROLLO`) y la rama de tu trabajo.
4. Asegúrate de incluir:
   - Un título claro.
   - Una descripción detallada de los cambios realizados.

#### **Plantilla sugerida para el PR:**
```markdown
### Descripción
Describe aquí los cambios realizados en el código.

### Tipo de cambio
- [ ] Nueva funcionalidad
- [ ] Corrección de errores
- [ ] Tareas de mantenimiento
- [ ] Mejora de funcionalidad existente
- [ ] Refactorización
- [ ] Documentación

### ¿Cómo probar los cambios?
Proporciona instrucciones para verificar los cambios realizados.
```

### **5. Revisar y fusionar**
Una vez creado el PR:
1. Notifica al equipo para que lo revise.
2. Realiza los ajustes necesarios basados en los comentarios.
3. Espera las aprobaciones requeridas antes de realizar el merge.

#### **Reglas de aprobación:**
- Al menos un revisor debe aprobar el PR.

---

## Buenas prácticas
1. **Commits pequeños y frecuentes:** Divide los cambios grandes en commits más pequeños para facilitar la revisión.
2. **Revisar antes de solicitar merge:** Asegúrate de que tu código esté limpio y funcional antes de crear el PR.
3. **Evitar conflictos:** Mantén tu rama actualizada con la rama base (por ejemplo, `DESARROLLO`).
   ```bash
   git pull origin DESARROLLO
   ```
4. **Documentar los cambios:** Si agregas o modificas funcionalidades importantes, actualiza también la documentación asociada.

---

## Notas finales
Cumplir con estas pautas asegura que el desarrollo sea organizado y colaborativo. Si tienes dudas, no dudes en consultar con el equipo o crear un issue en el repositorio.

