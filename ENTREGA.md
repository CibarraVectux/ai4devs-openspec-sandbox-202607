Entrega 1)
PS C:\ai4devs-openspec-sandbox-202607> openspec --version
1.6.0

PS C:\ai4devs-openspec-sandbox-202607> ls -R openspec/
    Directorio: C:\ai4devs-openspec-sandbox-202607\openspec


Mode                 LastWriteTime         Length Name                                                                   
----                 -------------         ------ ----                                                                   
d-----        13-07-2026     18:05                changes                                                                
d-----        13-07-2026     18:05                specs                                                                  
-a----        13-07-2026     18:05            573 config.yaml                                                            

    Directorio: C:\ai4devs-openspec-sandbox-202607\openspec\changes

Mode                 LastWriteTime         Length Name                                                                   
----                 -------------         ------ ----                                                                   
d-----        13-07-2026     18:05                archive  

Entrega 2)
## Micro-tarea

Crear una función que multiplique dos números sin utilizar el operador de multiplicación.

### Pilar 1 — Herramienta

Utilizaré **Codex desde Visual Studio Code**, apoyado por **OpenSpec** para definir la solución antes de implementarla.

Tecnologías:

* OpenSpec para documentar requisitos, diseño y tareas.
* Python para desarrollar la función.
* Pytest para ejecutar las pruebas.
* Github para controlar los cambios.

Comandos iniciales:

```bash
npm install -g @fission-ai/openspec@latest
openspec init
```

---

### Pilar 2 — Contexto

Se necesita implementar una función llamada `multiplicar` que reciba dos números enteros y retorne el resultado de su multiplicación.

Restricciones:

* No utilizar el operador `*`.
* No utilizar `*=`.
* No utilizar funciones que realicen internamente la multiplicación, como `math.prod`, `numpy.multiply`, `eval` o `exec`.
* La solución debe realizarse mediante sumas repetidas.
* Debe funcionar con números positivos, negativos y cero.
* El código debe ser simple, legible y estar acompañado de pruebas automatizadas.

Firma esperada:

```python
def multiplicar(numero_a: int, numero_b: int) -> int:
```

Criterios de aceptación:

```text
multiplicar(3, 4) devuelve 12
multiplicar(5, 0) devuelve 0
multiplicar(-3, 4) devuelve -12
multiplicar(3, -4) devuelve -12
multiplicar(-3, -4) devuelve 12
multiplicar(1, 7) devuelve 7
```

La tarea estará terminada cuando:

1. La función cumpla todos los casos definidos.
2. No exista ningún operador de multiplicación en la implementación.
3. Todas las pruebas automatizadas pasen correctamente.
4. La solución incluya manejo apropiado del signo.

---

### Pilar 3 — Prompt

```text
/opsx:propose crear-funcion-multiplicar-sin-operador

Crea una propuesta OpenSpec para implementar en Python una función llamada
multiplicar(numero_a: int, numero_b: int) -> int.

La función debe calcular el producto de dos números enteros sin utilizar el
operador de multiplicación, el operador de asignación multiplicativa ni
funciones externas que realicen la multiplicación.

La implementación debe utilizar sumas repetidas y manejar correctamente:

- Números positivos.
- Números negativos.
- Dos números negativos.
- Cero.
- El valor uno.

Genera los siguientes artefactos OpenSpec:

1. proposal.md con el objetivo, alcance y restricciones.
2. specs/calculo-multiplicacion/spec.md con los requisitos y escenarios
   GIVEN, WHEN y THEN.
3. design.md explicando el algoritmo de sumas repetidas y el manejo de signos.
4. tasks.md con las tareas de implementación y pruebas.

Incluye pruebas unitarias con pytest para los siguientes casos:

- multiplicar(3, 4) debe devolver 12.
- multiplicar(5, 0) debe devolver 0.
- multiplicar(-3, 4) debe devolver -12.
- multiplicar(3, -4) debe devolver -12.
- multiplicar(-3, -4) debe devolver 12.

No implementes todavía la solución. Primero genera la propuesta y los
artefactos OpenSpec para que puedan ser revisados.
```

Después de revisar la propuesta:

```text
/opsx:apply
```

Para verificar el resultado:

```text
/opsx:verify
```

Finalmente, para cerrar y archivar el cambio:

```text
/opsx:archive
```
Entrega 3)Observaciones de la exploración de OpenSpec
La verdad es que nunca había utilizado OpenSpec, es mi primera vez y de a poco iré conociendolo.