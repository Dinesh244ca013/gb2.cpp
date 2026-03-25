#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter number of frames: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Sending Frame " << i << endl;

        char ack;
        cout << "ACK received? (y/n): ";
        cin >> ack;

        if (ack == 'y') {
            cout << "Frame " << i << " acknowledged\n";
        } else {
            cout << "Frame " << i << " lost. Resending...\n";
            i--; // resend same frame
        }
    }
    return 0;
}