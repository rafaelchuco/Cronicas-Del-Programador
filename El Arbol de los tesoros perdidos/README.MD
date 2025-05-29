# 🏴‍☠️⚓ LA LEYENDA DEL ÁRBOL DEL TESORO PERDIDO ⚓🏴‍☠️

*Una épica aventura en los Siete Mares Digitales donde los datos navegan como corsarios*

---

## 🗺️ PRÓLOGO: EL MAPA DEL CÓDIGO PERDIDO 🗺️

En las aguas traicioneras del **Mar de los Algoritmos**, donde las estructuras de datos surcan las olas como barcos fantasma y los bucles infinitos devoran a los navegantes incautos, se cuenta la leyenda del **Árbol del Tesoro Perdido** 🌴💰. 

Este no es un árbol común, sino un **mapa viviente** que organiza los tesoros más valiosos del océano digital, donde cada nodo es un **corsario guardián** que protege cofres llenos de valores dorados...

---

## ⚓ CAPÍTULO I: LA TRIPULACIÓN DE LOS NODOS CORSARIOS ⚓

### *El Reclutamiento de los TreeNode Piratas*

En el puerto más peligroso del Caribe Digital, el **Capitán Constructor** recluta a sus primeros corsarios:

```python
class TreeNode:
    def __init__(self, value):
        self.value = value        # 💰 El cofre del tesoro personal
        self.left = None          # ⬅️ Ruta hacia la Isla de los Menores
        self.right = None         # ➡️ Sendero a la Bahía de los Mayores
```

🏴‍☠️ **Secretos del Corsario**: Cada `TreeNode` es un **Pirata Guardián** que posee:
- **💰 Value**: Su cofre personal lleno de monedas doradas
- **⬅️ Left**: El mapa hacia la **Isla de los Tesoros Menores** (valores más pequeños)
- **➡️ Right**: La brújula hacia la **Bahía de los Tesoros Mayores** (valores más grandes)

---

## 🏴‍☠️ CAPÍTULO II: EL CAPITÁN DEL ÁRBOL PIRATA 🏴‍☠️

### *La Coronación del BinarySearchTree como Rey de los Mares*

De las profundidades del océano emerge el legendario **Capitán BinarySearchTree**:

```python
class BinarySearchTree:
    def __init__(self):
        self.root = None  # 🌴 La isla principal donde comenzó todo
```

⚔️ **La Ley del Mar**: El `BinarySearchTree` es el **Capitán Supremo** que mantiene el orden en alta mar:
- Los tesoros menores navegan hacia **babor** (izquierda) ⬅️
- Los tesoros mayores surcan hacia **estribor** (derecha) ➡️
- ¡Cualquier pirata que desobedezca esta ley camina por la plancha! 🪦

---

## ⚔️ CAPÍTULO III: EL ABORDAJE Y RECLUTAMIENTO DE NUEVOS PIRATAS ⚔️

### *La Estrategia de Inserción Naval*

El Capitán ejecuta su táctica maestra para reclutar nuevos corsarios:

```python
def insert(self, value):
    if self.root is None:
        self.root = TreeNode(value)  # 🌴 La primera isla se convierte en base
    else:
        self._insert_recursive(self.root, value)  # 🌊 Navegación recursiva
```

🗺️ **Táctica Revelada**: 
- Si los **mares están vacíos** como el Triángulo de las Bermudas, el nuevo pirata se convierte en el **Capitán de la Isla Principal** 👑
- Si ya hay una flota establecida, se inicia la **Navegación Recursiva** para encontrar el puerto perfecto

### *La Navegación Recursiva: El Arte de Surcar los Mares Infinitos*

```python
def _insert_recursive(self, node, value):
    if value < node.value:
        if node.left is None:
            node.left = TreeNode(value)  # ⬅️ Anclaje en la Isla de los Menores
        else:
            self._insert_recursive(node.left, value)  # 🌊 Navegación hacia babor
    else:
        if node.right is None:
            node.right = TreeNode(value)  # ➡️ Desembarco en la Bahía de los Mayores
        else:
            self._insert_recursive(node.right, value)  # ⛵ Navegación hacia estribor
```

🌊 **El Arte de la Navegación Recursiva**: Esta técnica permite que el barco:
- **Divida** el océano en rutas más pequeñas
- **Conquiste** cada isla por separado
- **Combine** todos los territorios en un imperio pirata perfecto

---

## 🗺️ CAPÍTULO IV: LA CONSTRUCCIÓN DEL IMPERIO DESDE LA NADA 🗺️

### *El Gran Reclutamiento Masivo*

```python
def build_from_list(self, values):
    for value in values:
        self.insert(value)  # 🏴‍☠️ Cada valor se convierte en un nuevo corsario
```

⚓ **El Gran Plan**: Este ritual toma una **tripulación desordenada** de valores y los **entrena uno por uno** como corsarios disciplinados, creando un **imperio pirata perfectamente organizado** desde el caos más absoluto.

---

## 💰 CAPÍTULO V: LA BÚSQUEDA DEL TESORO EN EL RANGO DORADO 💰

### *La Misión Suprema: La Caza del Tesoro por Rango*

Llega el momento de la **Gran Expedición**, la misión más peligrosa que todo pirata sueña:

```python
def range_query(self, min_val, max_val):
    """💰 La expedición que encuentra todos los tesoros en el rango dorado"""
    treasure_chest = []  # 🏴‍☠️ El cofre donde guardaremos todo el botín
    
    def navigate_islands(current_pirate):
        if not current_pirate:
            return  # 🌊 Si llegamos a aguas vacías, regresamos al barco
        
        # ⬅️ Solo exploramos la Isla de los Menores si puede haber tesoros
        if current_pirate.value > min_val:
            navigate_islands(current_pirate.left)
        
        # 💎 Si el tesoro del pirata actual está en nuestro rango, lo saqueamos
        if min_val <= current_pirate.value <= max_val:
            treasure_chest.append(current_pirate.value)
        
        # ➡️ Solo navegamos a la Bahía de los Mayores si vale la pena
        if current_pirate.value < max_val:
            navigate_islands(current_pirate.right)
    
    navigate_islands(self.root)  # 🌴 Comenzamos desde la Isla Principal
    return treasure_chest  # 🏴‍☠️ Entregamos todo el botín saqueado
```

🏴‍☠️ **Las Tres Reglas de Oro del Saqueo**:

1. **⬅️ Exploración Inteligente de Babor**: Solo navega hacia la Isla de los Menores si `pirate.value > min_val`
2. **💰 Saqueo Selectivo**: Solo roba tesoros que cumplan `min_val ≤ treasure ≤ max_val`
3. **➡️ Expedición Sabia a Estribor**: Solo surca hacia la Bahía de los Mayores si `pirate.value < max_val`

⚔️ **El Secreto del Saqueo Perfecto**: Esta táctica usa el **Recorrido de Islas Ordenado**, una técnica legendaria que visita a cada pirata en **orden ascendente de riqueza**, aprovechando la organización natural del imperio para **evitar expediciones innecesarias** y encontrar tesoros con la eficiencia de un corsario veterano.

---

## 🧭 CAPÍTULO VI: LAS CINCO EXPEDICIONES LEGENDARIAS 🧭

### *Las Misiones que Probaron el Valor de la Flota*

```python
def test_range_query():
    # 🏴‍☠️ Expedición 1: El Archipiélago de los Siete Corsarios
    fleet1 = BinarySearchTree()
    fleet1.build_from_list([7, 3, 11, 1, 5, 9, 13])
    print("⚔️ Expedición 1:", fleet1.range_query(5, 10) == [5, 7, 9])  # ✅ Botín: [5, 7, 9]
    
    # 🏴‍☠️ Expedición 2: Las Cuatro Islas del Tesoro Completo
    fleet2 = BinarySearchTree()
    fleet2.build_from_list([6, 4, 8, 2])
    print("⚔️ Expedición 2:", fleet2.range_query(1, 10) == [2, 4, 6, 8])  # 🌊 Botín: [2, 4, 6, 8]
    
    # 🏴‍☠️ Expedición 3: El Mar de los Tesoros Inalcanzables
    fleet3 = BinarySearchTree()
    fleet3.build_from_list([20, 10, 30])
    print("⚔️ Expedición 3:", fleet3.range_query(1, 5) == [])  # 💀 Botín: [] (manos vacías)
    
    # 🏴‍☠️ Expedición 4: La Isla del Corsario Solitario
    fleet4 = BinarySearchTree()
    fleet4.build_from_list([15])
    print("⚔️ Expedición 4:", fleet4.range_query(10, 20) == [15])  # 🏝️ Botín: [15]
    
    # 🏴‍☠️ Expedición 5: El Rango de los Límites Perfectos
    fleet5 = BinarySearchTree()
    fleet5.build_from_list([15, 10, 20, 5, 25])
    print("⚔️ Expedición 5:", fleet5.range_query(10, 20) == [10, 15, 20])  # ⚓ Botín: [10, 15, 20]
```

---

## 🏴‍☠️ EPÍLOGO: EL CÓDIGO PIRATA REVELADO 🏴‍☠️

### *Los Secretos del Imperio de los Algoritmos Corsarios*

🦜 **¡Ahoy, valiente programador!** Has navegado por las aguas más traicioneras del **Mar de los Algoritmos** y has sido testigo de la **Leyenda del Árbol del Tesoro Perdido**. Permíteme compartir contigo el **Código Pirata** que acabas de descifrar:

#### ⚓ **La Anatomía de la Flota Digital**
- **TreeNode**: Los **Corsarios Inmortales** que protegen cofres dorados con sus vidas
- **BinarySearchTree**: El **Capitán Supremo** que mantiene la ley del mar: babor < centro < estribor

#### 🌊 **El Arte de la Navegación Recursiva**
- Cada inserción es una **expedición de reconocimiento**
- La recursión **surca los mares infinitos**, permitiendo que la flota se divida y conquiste territorio por territorio
- **Velocidad de navegación**: O(log n) en mares calmos, O(n) en la tormenta perfecta

#### 💰 **La Expedición Suprema: Range Query**
- **Recorrido Ordenado de Islas**: Visita corsarios en orden perfecto de riqueza
- **Saqueo Inteligente**: Evita expediciones a islas que no contienen el tesoro buscado
- **Eficiencia corsaria**: O(log n + k) donde k es el número de tesoros en el rango

#### ⚔️ **Los Tres Pilares del Imperio Pirata**
1. **Navegación Recursiva**: El arte de conquistar océanos dividiéndolos en mares más pequeños
2. **Estructura Binaria**: La ley universal donde cada decisión tiene exactamente dos rutas
3. **Orden Natural**: El código de honor que mantiene la flota en perfecta disciplina

### 🗺️ **La Profecía del Último Tesoro**

*"Cuando los datos se vuelvan caóticos como una tormenta en alta mar y los algoritmos parezcan tan imposibles como encontrar el Kraken, recuerda la leyenda del Árbol del Tesoro Perdido. Porque en su estructura simple yace el poder de organizar flotas enteras, y en su navegación recursiva habita la sabiduría de conquistar lo imposible dividiendo el océano en sus islas más pequeñas."*

**¡Que los vientos digitales llenen tus velas, intrépido corsario del código!** 🏴‍☠️⚓🦜

---

*Fin de la Leyenda*

**🏴‍☠️ Moral de la aventura**: Los Binary Search Trees no son solo estructuras de datos, son **imperios corsarios perfectamente organizados** que nos enseñan que la complejidad se conquista con **expediciones inteligentes** y **navegación recursiva**. ¡Cada línea de código es una orden del capitán que moldea el destino de la flota digital! ⚔️💰

**¡Arrr! ¡Que comience la siguiente expedición!** 🦜✨