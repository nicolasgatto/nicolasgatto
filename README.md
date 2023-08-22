<h1 align="center">Hi there, I'm Nicolás / Drandeds 👋</h1>

```cpp
class Developer {
public:
    Developer(const std::string& name, const std::string& title, int yearsOfExperience)
        : name(name), title(title), yearsOfExperience(yearsOfExperience) {}

    void displayInfo() const {
        std::cout << "Developer: " << name << std::endl;
        std::cout << "Title: " << title << std::endl;
        std::cout << "Years of experience: " << yearsOfExperience << std::endl;
    }

    void addSkill(const std::string& skill) {
        skills.push_back(skill);
    }

    void displaySkills() const {
        std::cout << "Skills:" << std::endl;
        for (const std::string& skill : skills) {
            std::cout << "- " << skill << std::endl;
        }
    }

private:
    std::string name;
    std::string title;
    int yearsOfExperience;
    std::vector<std::string> skills;
};

int main() {
    Developer developer("Nicolas Gatto", "Web Developer", 1);

    developer.addSkill("C++");
    developer.addSkill("JavaScript");
    developer.addSkill("Python");
    developer.addSkill("Vue");
    developer.addSkill("NodeJS");
    developer.addSkill("Firebase");
    developer.addSkill("MySQL/MongoDB");

    developer.displayInfo();
    
    developer.displaySkills();

    return 0;
}
```
