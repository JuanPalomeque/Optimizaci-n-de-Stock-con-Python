# Optimizacion de niveles de Stock 
# Fórmulas para operaciones con Stocks

# Defino
def Cantidad_Optima(C, D, H):
    """
    Cantidad económica de ordenes

    Argumentos:
    C: costo de la orden
    D: cantidad anual demandada
    H: costo de tener el producto
    """

    Q = (np.sqrt(2 * C * D / H))
    numero_de_ordenes = D / Q
    tiempo_entre_ciclos = 12 / number_of_orders
    AOC = D / Q * C
    AHC = Q / 2 * H
    ATC = AOC + AHC

    return [Q, numero_de_ordenes, tiempo_entre_ciclos, AOC, AHC, ATC]
