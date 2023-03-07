#include <iostream>
#include <string>
using namespace std;

class StringConverter {
private:
    string input_string;
public:
    StringConverter(string str) {
        input_string = str;
    }

    string toUpperCase() {
        string upper_str = input_string;
        for (int i = 0; i < upper_str.length(); i++) {
            upper_str[i] = toupper(upper_str[i]);
        }
        return upper_str;
    }
    string toLowerCase() {
        string lower_str = input_string;
        for (int i = 0; i < lower_str.length(); i++) {
            lower_str[i] = tolower(lower_str[i]);
        }
        return lower_str;
    }
};
int main() {
    string input_str;
    cout << "Enter a string: ";
    getline(cin, input_str);

    StringConverter converter(input_str);
    cout << "Uppercase string: " << converter.toUpperCase() << endl;
    cout << "Lowercase string: " << converter.toLowerCase() << endl;

    return 0;
}
