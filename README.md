# mari
def bin2(n, k):
    B = [[0 for x in range(k + 1)] for x in range(n + 1)]

    for i in range(n + 1):
        for j in range(min(i, k) + 1):

            if j == 0 or j == i:
                B[i][j] = 1
            else:
                B[i][j] = B[i - 1][j - 1] + B[i - 1][j]

    return B[n][k]

n = input ("Enter n:")
k = input ("Enter k:")
print("output B[" + str(int(n)) + "][" + str(int(k)) + "] is " + str(bin2(int(n), int(k))))
