# -#include <iostream>;
using namespace std;

void bouble() {
    int a[20], n;
    cout << "enter the size (0 < n < 20): ";
    cin >> n;
    cout << "enter the values:\n";
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }
    cout << "[";
    for (int i = 0; i < n; i++) {
        if (i == 0) cout << a[i];
        else cout << ", " << a[i] ;
    }
    cout << "]\n";
    for (int i = 1; i < n; ++i)
    {
        for (int j = 0; j < n - i; j++)
        {
            if (a[j] > a[j + 1])
            {
                // change
                int k = a[j];
                a[j] = a[j + 1];
                a[j + 1] = k;
            }
        }
    }
    cout << "[";
    for (int i = 0; i < n; i++) {
        if (i == 0) cout << a[i];
        else cout << ", " << a[i];
    }
    cout << "]\n";
}
void insertion() {
    int a[20], n;
    cout << "enter the size (0 < n < 20): ";
    cin >> n;
    cout << "enter the values:\n";
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }
    cout << "[";
    for (int i = 0; i < n; i++) {
        if (i == 0) cout << a[i];
        else cout << ", " << a[i];
    }
    cout << "]\n";
    for (int i = 1; i < n; i++) {
        for (int j = i; j > 0 && a[j - 1] > a[j]; j--) {
            //change
            int k = a[j - 1];
            a[j - 1] = a[j];
            a[j] = k;
        }
    }
    cout << "[";
    for (int i = 0; i < n; i++) {
        if (i == 0) cout << a[i];
        else cout << ", " << a[i];
    }
    cout << "]\n";
}

int main()
{
    cout << "choose a sort: " << endl << "1. bouble" << endl << "2. insertion\n";
    char k;
    bool b = false;
    while (b!=true) {
        cout << "cin: ";
        cin >> k;
        if ((k == '1') || (k == '2')) {
            switch (k) {
            case '1':
                bouble();
                break;
            case '2':
                insertion();
                break;
            }
            b = true;
        }
        else b = false;
    }
}
