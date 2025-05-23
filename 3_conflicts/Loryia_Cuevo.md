3.1. Preguntas
1. ¿Qué es un conflicto? Cuando ocurre? ¿Es bueno o malo?
    Ocurre cuando dos ramas modifican la misma parte de un archivo, ocurre durante un merge, rebase o cherry-pick. No es bueno ni malo.

2. ¿Se puede evitar un conflicto? ¿Cómo?
    Se puede evitar con buena comunicación, haciendo commits y pulls frecuentes, y evitando editar las mismas líneas en ramas distintas.


3.2. Ejercicio Práctico
1. Crear un archivo nombre_apellido.txt dentro de la carpeta 3.conflicts.


2.  Crear una nueva branch suprema a partir de la branch master. (Puede usar el comando git checkout -b suprema).
        >git checkout -b suprema
    Switched to a new branch 'suprema'

3. Moverse a la branch suprema. (Puede usar el comando git checkout).
        Se movió automáticamente.

4. Cambiar el contenido del archivo 3.conflicts/milanesa.txt donde dice lomo por pollo.


5. "Commitear" los cambios. (Puede usar el comando git commit -am "Cambio de lomo a pollo").
        >git commit -am "Cambio de lomo a pollo"
    [suprema f785ebc] Cambio de lomo a pollo
    1 file changed, 2 insertions(+)
    create mode 100644 3.conflicts/milanesa.txt

6. Moverse a la branch master. (Puede usar el comando git checkout).
        >git checkout master
    Switched to branch 'master'

7. Crear una nueva branch bife a partir de la branch master. (Puede usar el comando git checkout -b bife).
        >git checkout -b bife
    Switched to a new branch 'bife'

8. Moverse a la branch bife. (Puede usar el comando git checkout).
        Se movió automáticamente.

9. Cambiar el contenido del archivo 3.conflicts/milanesa.txt donde dice lomo por bife.


10. Haga un git diff master suprema y un git diff master bife. ¿Qué observa?
        git diff master suprema
    diff --git a/3.conflicts/milanesa.txt b/3.conflicts/milanesa.txt
    new file mode 100644
    index 0000000..1c57c4d
    --- /dev/null
    +++ b/3.conflicts/milanesa.txt
    @@ -0,0 +1,2 @@
    +pan rallado
    +pollo

11. Moverse a la branch master. Corra un git status, ¿qué observa?


12. Ejecute git merge bife. Funcionó?
        git merge bife
    Already up to date.

13. Ejecute git merge suprema. Funcionó?
        >git merge suprema
    Updating 7f9f56a..01d6b27
    Fast-forward
    3.conflicts/milanesa.txt | 2 ++
    1 file changed, 2 insertions(+)
    create mode 100644 3.conflicts/milanesa.txt

14. Ejecute git status. Que observa?


15. Vea el contenido del archivo 3.conflicts/milanesa.txt. ¿Qué observa?


16. Aborte el merge. (Puede usar el comando git merge --abort).


17. Vuelva a ejecutar git merge suprema.


18. Resuelva el conflicto manualmente.

