solution.cpp
#include <iostream>
#include <string>
#include <algorithm>
#include <vector>

// Function to count vowels in a string
int countVowels(const std::string &str) {
    int count = 0;
    std::string vowels = "aeiouAEIOU";
    
    for(char c : str) {
        if (vowels.find(c) != std::string::npos) {
            count++;
        }
    }
    return count;
}

// Function to reverse a string
std::string reverseString(const std::string &str) {
    std::string reversed = str;
    std::reverse(reversed.begin(), reversed.end());
    return reversed;
}

// Function to filter even numbers from an array
std::vector<int> filterEvenNumbers(const std::vector<int> &arr) {
    std::vector<int> evens;
    
    for(int num : arr) {
        if (num % 2 == 0) {
            evens.push_back(num);
        }
    }
    return evens;
}

int main() {
    // Testing countVowels
    std::cout << "Vowels in 'hello world': " << countVowels("hello world") << std::endl; // Output: 3
    std::cout << "Vowels in 'The quick brown fox': " << countVowels("The quick brown fox") << std::endl; // Output: 5
    std::cout << "Vowels in 'AEIOU': " << countVowels("AEIOU") << std::endl; // Output: 5
    std::cout << "Vowels in 'Python Programming': " << countVowels("Python Programming") << std::endl; // Output: 4

    // Testing reverseString
    std::cout << "Reversed 'hello': " << reverseString("hello") << std::endl; // Output: olleh
    std::cout << "Reversed 'JavaScript': " << reverseString("JavaScript") << std::endl; // Output: tpircSavaJ
    std::cout << "Reversed '12345': " << reverseString("12345") << std::endl; // Output: 54321
    std::cout << "Reversed 'A man a plan a canal Panama': " << reverseString("A man a plan a canal Panama") << std::endl; // Output: amanaP lanac a nalp a nam A

    // Testing filterEvenNumbers
    std::vector<int> result1 = filterEvenNumbers({1, 2, 3, 4, 5});
    std::cout << "Even numbers in {1, 2, 3, 4, 5}: ";
    for(int num : result1) std::cout << num << " "; // Output: 2 4
    std::cout << std::endl;
    
    std::vector<int> result2 = filterEvenNumbers({10, 15, 20, 25});
    std::cout << "Even numbers in {10, 15, 20, 25}: ";
    for(int num : result2) std::cout << num << " "; // Output: 10 20
    std::cout << std::endl;
    
    std::vector<int> result3 = filterEvenNumbers({7, 11, 13});
    std::cout << "Even numbers in {7, 11, 13}: ";
    for(int num : result3) std::cout << num << " "; // Output: (empty line)
    std::cout << std::endl;
    
    std::vector<int> result4 = filterEvenNumbers({0, -2, -4});
    std::cout << "Even numbers in {0, -2, -4}: ";
    for(int num : result4) std::cout << num << " "; // Output: 0 -2 -4
    std::cout << std::endl;

    return 0;
}

<!---
annet-ngoroi/annet-ngoroi is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
