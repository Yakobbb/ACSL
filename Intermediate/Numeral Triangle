def sumOfLastRows(s, d, r):
    start=str(s)
    delta=str(d)
    rows=r

    isStartNegative = False
    if start[0] == "-":
        isStartNegative = True
        start.replace("-", "")

    startDecimal = 0
    deltaDecimal = 0
    for i in range(1, len(start)+1):
        digit = int(start[-i])
        startDecimal += digit*(8**(i-1))
    if isStartNegative:
        startDecimal*=-1
    for i in range(1, len(delta)+1):
        digit = int(delta[-i])
        deltaDecimal += digit*(8**(i-1))

    #I now have all numbers in decimal, whether s is negative or not

    if rows == 0:
        print(0)
        return 0
    #above is an exception case: if the amount of rows is 0
    elif rows == 1:
        print(start)
        return int(start)
    #another exception case: if rows=1, just return s

    listOfLastRow = []
    for i in range(rows-1):
        listOfLastRow.clear()
        for m in range(0, i+2):
            startDecimal += deltaDecimal
            listOfLastRow.append(startDecimal)

    finalListOfLastRow = []
    for num in listOfLastRow:
        numInOctal = oct(num)
        finalListOfLastRow.append(int(numInOctal.replace("0o", "")))

    listToAdd = []
    for i in finalListOfLastRow:
        nums = list(str(i))
        for num in nums:
            listToAdd.append(int(num))

    finalSum = 0
    for i in listToAdd:
        finalSum+=i
    return(finalSum)
