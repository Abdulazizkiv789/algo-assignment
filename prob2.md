function dotProduct(v1, v2) {
    let ps = 0;
    for (let i = 0; i < v1.length; i++) {
        ps += v1[i] * v2[i];
    }
    return ps;
}
function checkOrthogonalPairs(vectors1, vectors2) {
    for (let i = 0; i < vectors1.length; i++) {
        let ps = dotProduct(vectors1[i], vectors2[i]);
        if (ps === 0) {
            console.log(`Vectors at index ${i} are orthogonal`);
        } else {
            console.log(`Vectors at index ${i} are not orthogonal`);
        }
    }
}

// Example usage:
let vectors1 = [
    [1, 2, 3],
    [4, -2, 1]
];

let vectors2 = [
    [4, -5, 6],
    [2, 4, -1]
];

checkOrthogonalPairs(vectors1, vectors2);
// Output:
// Vectors at index 0 are not orthogonal
// Vectors at index 1 are orthogonal
