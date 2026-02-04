# Assignment 3 – C++ Functions

This repository contains solutions to Assignment 3, which focuses on writing C++ functions that work with integers, strings, and lists (vectors).

---

## 1. Sum of Two Integers

```cpp
int sum(int x, int y) {
    return x + y;
}

int countVowels(const std::string& str) {
    int count = 0;
    for (char c : str) {
        char ch = tolower(c);
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            count++;
        }
    }
    return count;
}

double average(const std::vector<int>& numbers) {
    int sum = 0;
    for (int num : numbers) {
        sum += num;
    }
    return static_cast<double>(sum) / numbers.size();
}

std::string removeVowels(const std::string& sentence) {
    std::string result;
    for (char c : sentence) {
        char ch = tolower(c);
        if (!(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u')) {
            result += c;
        }
    }
    return result;
}

std::string longestString(const std::vector<std::string>& words) {
    std::string longest = words[0];
    for (const std::string& word : words) {
        if (word.length() > longest.length()) {
            longest = word;
        }
    }
    return longest;
}

double median(std::vector<int> numbers) {
    std::sort(numbers.begin(), numbers.end());
    int n = numbers.size();

    if (n % 2 == 0) {
        return (numbers[n / 2 - 1] + numbers[n / 2]) / 2.0;
    } else {
        return numbers[n / 2];
    }
}

std::vector<int> removeEvenNumbers(const std::vector<int>& numbers) {
    std::vector<int> result;
    for (int num : numbers) {
        if (num % 2 != 0) {
            result.push_back(num);
        }
    }
    return result;
}

std::vector<std::string> sortStrings(std::vector<std::string> words) {
    std::sort(words.begin(), words.end());
    return words;
}

int sumOfList(const std::vector<int>& numbers) {
    int sum = 0;
    for (int num : numbers) {
        sum += num;
    }
    return sum;
}

std::vector<std::string> reverseStrings(const std::vector<std::string>& words) {
    std::vector<std::string> result = words;
    for (std::string& word : result) {
        std::reverse(word.begin(), word.end());
    }
    return result;
}
