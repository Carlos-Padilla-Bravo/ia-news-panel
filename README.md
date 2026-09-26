# Panel diario de noticias de inteligencia artificial

**Panel en vivo: https://carlos-padilla-bravo.github.io/ia-news-panel/**

Una selección diaria de cinco noticias de inteligencia artificial, verificada una por una
en su fuente original y clasificada con criterios fijos. La serie empezó en julio de 2026
y se actualiza todas las noches.

## Qué hay acá

Este repositorio contiene solo el panel ya generado (`index.html`), que se publica por
GitHub Pages. El archivo es autocontenido: trae los datos, los gráficos y los filtros
dentro, sin dependencias externas.

La serie completa vive en una planilla que no está en este repositorio. Lo que se ve acá
es la salida, no la fuente.

## Cómo se arma la selección

Cinco noticias por día, publicadas ese día. Dos de ellas son lanzamientos de productos,
modelos o herramientas; las otras tres cubren el resto del sector: regulación y fallos
judiciales, financiamiento y adquisiciones, incidentes de seguridad, fallas de
alineamiento, infraestructura, resultados de investigación y efectos sobre el trabajo y
la sociedad. El tope de dos lanzamientos es deliberado: un día contado solo con
lanzamientos deja fuera la mitad de lo que importa.

Tres reglas sostienen la serie:

- **Verificación en fuente.** Cada noticia se abre en el sitio que la publicó y ahí se
  confirma la fecha. Los agregadores diarios sirven para encontrar candidatas y nunca
  como fuente: fechan mal de forma sistemática. Si la página no abre o no declara la
  fecha, la noticia se descarta, aunque sea buena.
- **Un dominio, una noticia.** Dentro de un mismo día no se repite el medio. Dos medios
  que cuentan el mismo hecho son una sola noticia.
- **Informar, no opinar.** El resumen reproduce lo que dice la fuente: qué pasó, quién lo
  hizo, las cifras que entrega y por qué importa según ella misma. Cuando una empresa
  afirma que su modelo supera a otros, se escribe como afirmación de parte.

Es preferible un día con cuatro noticias verificadas que uno con cinco donde una se dio
por buena sin comprobar.

## Cómo se clasifica

Cada noticia lleva seis campos, todos de valores cerrados:

| Campo | Qué responde |
| --- | --- |
| Tema | De qué habla la noticia |
| Tipo de hecho | Qué clase de hecho es, con independencia del tema |
| Dirección | Si deja al actor mejor, peor o igual |
| Actor principal | La organización protagonista |
| País o región | Dónde ocurre el hecho |
| Estado del hecho | Si está consumado, en curso o solo anunciado |

Tema y tipo son dimensiones distintas y se llenan por separado. Una ronda de inversión en
una empresa de robótica es tema «Robótica e IA física» y tipo «Financiamiento e
inversión»; un modelo nuevo es tema «Producto y modelos» y tipo «Lanzamiento».

## Quién lo hace

Carlos Padilla Bravo. Doctor en ciencias agrarias, trabaja en ciencia de datos,
estrategia e innovación, y hace docencia universitaria en marketing, estrategia e
investigación de mercado.

## Licencia

Dos licencias, porque el repositorio mezcla dos cosas distintas.

**El código del tablero** (el JavaScript y el CSS que hacen funcionar los filtros, los
gráficos y el modo claro/oscuro) está bajo licencia MIT. Ver [LICENSE](LICENSE).

**Los datos y los resúmenes** (la selección diaria, los resúmenes redactados y la
clasificación) están bajo [Creative Commons Atribución 4.0
Internacional](https://creativecommons.org/licenses/by/4.0/deed.es). Puedes copiarlos,
redistribuirlos y adaptarlos, incluso con fines comerciales, citando la autoría y
enlazando a este repositorio.

Un límite que conviene aclarar: esas licencias cubren lo que es propio de este proyecto.
**No se extienden a los titulares, textos ni contenidos originales de los medios
enlazados**, que pertenecen a sus respectivos autores y editores. Las URL de origen están
en cada ficha justamente para que el crédito quede donde corresponde.
