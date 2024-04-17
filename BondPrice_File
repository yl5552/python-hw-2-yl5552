import numpy as np

def getBondPrice(y, face, couponRate, m, ppy=1):
    t = np.arange(1, m * ppy + 1)
    pv = (1 + y / ppy) ** -t
    cf = couponRate * face / ppy
    pvcf = pv * cf

    bond_price = sum(pvcf) + pv[-1] * face
    return bond_price

round(getBondPrice(.03, 2000000, .04, 10,  1)) == 2170604
round(getBondPrice(.03, 2000000, .04, 10,  2)) == 2171686
