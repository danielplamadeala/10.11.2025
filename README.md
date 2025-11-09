#include <iostream>
using namespace std;

int main() {
    int n, m, A[20], B[20];

    cout << "Numarul de elemente din multimea A: ";
    cin >> n;
    cout << "Elementele multimii A: ";
    for (int i = 0; i < n; i++)
        cin >> A[i];

    cout << "Numarul de elemente din multimea B: ";
    cin >> m;
    cout << "Elementele multimii B: ";
    for (int i = 0; i < m; i++)
        cin >> B[i];

    // Reuniunea
    cout << "Reuniune: ";
    for (int i = 0; i < n; i++)
        cout << A[i] << " ";

    for (int i = 0; i < m; i++) {
        bool gasit = false;
        for (int j = 0; j < n; j++)
            if (B[i] == A[j]) gasit = true;
        if (!gasit) cout << B[i] << " ";
    }
    cout << endl;

    // Intersecția
    cout << "Intersectie: ";
    for (int i = 0; i < n; i++)
        for (int j = 0; j < m; j++)
            if (A[i] == B[j])
                cout << A[i] << " ";
    cout << endl;

    // Diferența A \ B
    cout << "Diferenta A\\B: ";
    for (int i = 0; i < n; i++) {
        bool gasit = false;
        for (int j = 0; j < m; j++)
            if (A[i] == B[j]) gasit = true;
        if (!gasit) cout << A[i] << " ";
    }
    cout << endl;

    // Diferența B \ A
    cout << "Diferenta B\\A: ";
    for (int i = 0; i < m; i++) {
        bool gasit = false;
        for (int j = 0; j < n; j++)
            if (B[i] == A[j]) gasit = true;
        if (!gasit) cout << B[i] << " ";
    }
    cout << endl;

    return 0;
}
