2.1. Preguntas
1. ¿Qué es un branch?
Es una rama independiente del código principal donde puedes hacer cambios sin afectar el proyecto principal.

2. ¿Por qué pueden ser útiles los branches?
Permiten desarrollar nuevas funciones o corregir errores sin alterar el código principal.

3. ¿Cómo se crea una branch?
git branch nombre-rama

4. ¿Cómo se cambia a una branch?
git checkout nombre-rama

5. ¿Cómo se elimina una branch?
git branch -d nombre-rama

6. ¿Cómo se crea una branch y se cambia a ella en un solo paso?
git checkout -b nombre-rama

7. ¿Qué es un merge?
Es la acción de unir los cambios de una rama con otra.

8. ¿Cómo se realiza un merge?
git merge nombre-rama

9. ¿Que es un tag?
Es una etiqueta que marca versiones específicas del código, como un punto de referencia.

10. ¿Cómo se crea un tag?
git tag nombre-tag


2.2. Ejercicio Práctico
Antes de continuar con el ejercicio, se debe agregar un alias para facilitar la visualización de los branches.

git config --global alias.graph "log --all --graph --decorate --oneline"

# Pruebe el comando
git graph
1. [] Crear una branch experimento. (Puede usar el comando git branch experimento master).
2. Moverse a la branch experimento. (Puede usar el comando git checkout).
3. Verificar que se encuentra en la branch ejercicio_2. (Puede usar el comando git branch).
4. Agregarle el condimento albahaca arriba del queso al archivo 2.branchs/pizza.txt y "commitee" los cambios.
5. Agregarle el condimento oregano arriba de la albahaca al archivo 2.branchs/pizza.txt y "commitee" los cambios.
6. Correr el comando git graph y observar el resultado. ¿Qué observa?
7. Vuelva a la branch master.
8. Crear una branch anana. (Puede usar el comando git checkout -b anana).
9. Agregarle el condimento anana debajo del queso al archivo 2.branchs/pizza.txt y "commitee" los cambios.
        git commit -m "pizzaoreganoanana"
    [main 9656bb3] pizzaoreganoanana
    1 file changed, 6 insertions(+)
    create mode 100644 2.branchs/pizza.txt

10. Correr el comando git graph y observar el resultado. ¿Qué observa?
        git graph
    * 9656bb3 (HEAD -> main) pizzaoreganoanana

11. Vuelva a la branch master.
12. Agregue el condimento cebolla debajo de la salsa al archivo 2.branchs/pizza.txt y "commitee" los cambios.
        >git commit -m "cebollabajosalsa"
    [main 867c64a] cebollabajosalsa
    1 file changed, 1 insertion(+)

13. Correr el comando git graph y observar el resultado. ¿Qué observa?
        >git graph
    * 867c64a (HEAD -> main) cebollabajosalsa

14. Haga un merge de la branch anana a la branch master. (Puede usar el comando git merge anana).
        git merge anana

15. Correr el comando git graph y observar el resultado. ¿Qué observa?

16. ¿Qué branches están "mergeadas" a master? (Puede usar el comando git branch --merged).
17. Haga un merge de la branch experimento a la branch master. (Puede usar el comando git merge experimento).
18. Correr el comando git graph y observar el resultado. ¿Qué observa?
19. ¿Tuvo que hacer un merge manual, o git lo hizo automáticamente? ¿Por qué?
20. ¿Qué branches están "mergeadas" a master? (Puede usar el comando git branch --merged).
21. Elimine la branch anana. (Puede usar el comando git branch -d anana).
        git branch -d anana
    Deleted branch anana (was 7f9f56a).

22. Elimine la branch experimento. (Puede usar el comando git branch -d experimento).
        git branch -d experimento
    Deleted branch experimento (was 7f9f56a).

23. ¿Qué branches están "mergeadas" a master? (Puede usar el comando git branch --merged).
24. Correr el comando git graph y observar el resultado. ¿Qué observa?
25. Crear un tag pizza en el último commit. (Puede usar el comando git tag -a pizza -m "Receta de la pizza."").
26. Ver los tags creados. (Puede usar el comando git tag).
        git tag
    pizza
27. Ver el tag pizza. (Puede usar el comando git show pizza).
        git show pizza
    tag pizza
    Tagger: loreiish <loreishush@gmail.com>
    Date:   Wed May 21 17:19:20 2025 +0200