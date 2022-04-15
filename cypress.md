
# CURSO DE CYPRESS.

    "use stric" <--- standard en cada page.


## COMANDOS BÁSICOS.

    *cy.visit()* Visitar página web o aplicación.
    *cy.reload* Recargar.
    *cy.go("back")* Ejemplo de ir hacia atrás.
    *cy.get("selector")* Obtener selector.
    *cy.contains("p","texto")* Ejemplo de selector y texto.
    *cy.contains("texto")* Ejemplo para un input.

## ACCIONES.

    *click()* Click.
    *dbclick()* Doble Click.
    *type()* Escribir.
    *clear()* Limpiar.
    *check()* Chequear (checkbox).
    *uncheck()* Deschequear.
    *select()* Seleccionar.
    *cy.wait(3000)* Ejemplo de una espera de 3 segs.

## ASERTIONS. Algunos Ejemplos.

    *cy.get("Error msg").should("no.exist")*
    *cy.get("Error msg").should("be.visible")*
    *cy.contains("a","dashboard").should("be.visible")*
    
## HOOKS.

    *describe()* Descripción de la prueba.
    *context()* Contexto
    *it()* Acción del test
    *before()* Antes de todo.
    *beforeeach()* Antes de cada test(acción global por cada test)
    *aftereach()* Despues de cada test.
    *only()* Sólo la acción seleccionada.
    *skip()* Saltar.

    hooks --> Pueden entrar los Assertions. 
    Se pueden agregar al json --> "Standard" {} "global" {}


## PLANTILLA DE UN TEST EN CYPRESS.

///////
        "use strict"
            describe ("Prueba Automatizada", () =>{
            it ("test de ejemplo", () => {código del test})
        }
        );

//////

## CONFIGURAR AUTOCOMPLETADO.

    tsconfig.json  --> Dentro del cypress.
    "Code completion"

## DEBUG O DEPURACIÓN.

    *.debug()*
    package.json [headless testing]-consola --> copiar --> cypress open --> cypress run ----> test

## COMANDOS PERSONALIZADOS.

    Código repetido --> support --> common.js ---> cypress Commands.add(..) ---> cv.loginuser(userdata) <---se utilizan variables abstraidas.
    *cy.screenshot()* Para capturas.
    *blackout* Negro para proteger datos.
    *stubs* Simula, sustituye comportamiento.
    *spies* Interviene en los llamados.
    *clocks* Altera programaticamente la hora y fecha del entorno.

