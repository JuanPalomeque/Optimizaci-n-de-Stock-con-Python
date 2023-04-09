# Optimizacion-de-Stock-con-Python
Fórmulas para operaciones con Stocks

# Defino
def Cantidad_Optima(S, D, H):
    """
    Economic Order Quantity

    Arguments:
    S: ordering cost
    D: annual quantity demanded
    H: holding cost per unit

    Q = (np.sqrt(2 * S * D / H))
    number_of_orders = D / Q
    time_between_cycles = 12 / number_of_orders
    AOC = D / Q * S
    AHC = Q / 2 * H
    ATC = AOC + AHC

    return [Q, number_of_orders, time_between_cycles, AOC, AHC, ATC]
