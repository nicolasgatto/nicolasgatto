```cpp
#include <iostream>
#include <vector>
#include <map>

class Developer {
public:
    Developer(const std::string& name, const std::string& title, int yearsOfExperience)
        : name(name), title(title), yearsOfExperience(yearsOfExperience) {}

    void displayInfo() const {
        std::cout << "Developer: " << name << std::endl;
        std::cout << "Title: " << title << std::endl;
        std::cout << "Years of experience: " << yearsOfExperience << std::endl;
    }

    void addSkill(const std::string& category, const std::string& skill) {
        if (std::find(categoriesOrder.begin(), categoriesOrder.end(), category) == categoriesOrder.end()) {
            categoriesOrder.push_back(category);
        }
        skills[category].push_back(skill);
    }

    void displaySkills() const {
        std::cout << "Skills:" << std::endl;
        for (const std::string& category : categoriesOrder) {
            std::cout << category << ":" << std::endl;
            for (const std::string& skill : skills.at(category)) {
                std::cout << "- " << skill << std::endl;
            }
        }
    }

private:
    std::string name;
    std::string title;
    int yearsOfExperience;
    std::map<std::string, std::vector<std::string>> skills;
    std::vector<std::string> categoriesOrder;
};

int main() {
    Developer developer("Nicolas Gatto", "Web Developer", 1);

    developer.addSkill("Front-end", "Vue.js");
    developer.addSkill("Front-end", "JavaScript");
    developer.addSkill("Front-end", "JQuery");
    developer.addSkill("Front-end", "Boostrap");
    developer.addSkill("Back-end", "Node.js");
    developer.addSkill("Back-end", "PHP");
    developer.addSkill("Database", "MySQL");
    developer.addSkill("Database", "Firebase");
    developer.addSkill("Cybersecurity", "Metasploit");
    developer.addSkill("Cybersecurity", "Burp Suite");
    developer.addSkill("Cybersecurity", "Nmap");
    developer.addSkill("Cybersecurity", "Wireshark");
    developer.addSkill("Cybersecurity", "OWASP Zap");
    developer.addSkill("Cybersecurity", "BlackArch");
    developer.addSkill("Programming", "C++");
    developer.addSkill("Programming", "Python");
    developer.addSkill("Programming", "Flutter");

    developer.displayInfo();

    developer.displaySkills();

    return 0;
}
```

## Curriculum Vitae / Resume

### English

[English Resume (PDF)](https://github.com/nicolasgatto/nicolasgatto/blob/main/Nicolas%20Gatto%20Resume%20ENG.pdf)

### Español

[Currículum Español (PDF)](https://github.com/nicolasgatto/nicolasgatto/blob/main/Nicolas%20Gatto%20Resume%20ESP.pdf)
