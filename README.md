El modelo resuelve un escenario de logística corporativa donde se requiere abastecer a 2 centros de distribución (Denver y Miami) desde 3 plantas automotrices (Los Ángeles, Detroit y Nueva Orleans). El algoritmo procesa:
Capacidades de Oferta: Límite máximo de unidades que cada planta puede producir en el trimestre.
Requerimientos de Demanda: Unidades exactas exigidas por cada centro de distribución.
Matriz de Costos: Costo de transporte por unidad basado en la distancia en millas (8 centavos por milla) entre cada nodo de la red.

Características Principales 
Modelado Matricial con SciPy: Transformación del problema algebraico en matrices de restricciones de igualdad ($A_{eq}, b_{eq}$) para resolver la función objetivo mediante el algoritmo *Highs*.
Modelado Declarativo con PuLP: Construcción de un modelo de programación entera (`Integer`) más legible y escalable, definiendo dinámicamente diccionarios de variables, restricciones de sumatoria iterativa y funciones objetivo minimizadoras.
Validación Cruzada: Resolución del mismo problema utilizando dos motores matemáticos distintos (`SciPy` y `PuLP`) para auditar y confirmar que el costo total mínimo ($313,200.00) y la matriz de asignación sean idénticos y matemáticamente precisos.


Este tipo de modelado es directamente aplicable a la gestión de cadenas de suministro, asignación de recursos corporativos y evaluación de riesgos logísticos, permitiendo a las organizaciones tomar decisiones basadas en datos para maximizar sus márgenes de utilidad.
