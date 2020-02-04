# HigherOrderFunctionPlayground

import UIKit

let numberArray = [5,8,2,9,12,7,3,10,1,15,20]

//------------ Sorting -------------

/// Ascending order array
let ascendingArray = numberArray.sorted()
print("ascendingArray \(ascendingArray)")

/// Descending order array
let descendingArray = numberArray.sorted(by: {(a,b) -> Bool in
    return a > b
})
print("descendingArray \(descendingArray)")

/// Even number First
let evenOddNumber = numberArray.sorted(by: {(a, b) -> Bool in
    return a % 2 == 0
})
print("evenOddNumber \(evenOddNumber)")

/// Closure Syntax
let descending = numberArray.sorted(by: >)
print("descending \(descending)")


//------------ Map ---------------

/// Simple map function to convert number to string
let mapString = numberArray.map({(a) -> String in
    return String(a)
})
print("mapString \(mapString)")

/// Inline syntax with clousers
let inlineSyntaxMap = numberArray.map({String($0)})
print("inlineSyntaxMap \(inlineSyntaxMap)")

//------------ Filter ---------------

/// Less than number
let lessThanNumber = numberArray.filter({ (a) ->Bool in
    return a < 5
})
print("lessthanNumber \(lessThanNumber)")

///Inline Syntax

let inlineSyntaxFilter = numberArray.filter{ ($0 < 5)}
print("inlineSyntaxFilter \(inlineSyntaxFilter)")


//------------ Reduce ---------------


/// Sum of all numbers
let sumOfNumber = numberArray.reduce("", {(result, a) -> String in
    return result + String(a)
})
print("SumOfNumber \(sumOfNumber)")

