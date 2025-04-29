function sumOfDistinctElements(set1, set2) {
    let sum = 0;

    // Check elements in set1 not in set2
    for (let i = 0; i < set1.length; i++) {
        let found = false;
        for (let j = 0; j < set2.length; j++) {
            if (set1[i] === set2[j]) {
                found = true;
                break;
            }
        }
        if (!found) {
            sum += set1[i];
        }
    }

    // Check elements in set2 not in set1
    for (let j = 0; j < set2.length; j++) {
        let found = false;
        for (let i = 0; i < set1.length; i++) {
            if (set2[j] === set1[i]) {
                found = true;
                break;
            }
        }
        if (!found) {
            sum += set2[j];
        }
    }

    return sum;
}

// Example usage:
let set1 = [3, 1, 7, 9];
let set2 = [2, 4, 1, 9, 3];
console.log("Sum of distinct elements:", sumOfDistinctElements(set1, set2)); // Output: 13
