```go
// Dang Nhut Nguyen - 915080
// Software Developer & AI Enthusiast
// Profile Views: https://komarev.com/ghpvc/?username=dangnhutnguyen

package main

import (
    "fmt"
    "strings"
)

type Organization struct {
    Name      string
    Position  string
    Projects  []string
    Teammates []string
}

type AboutMe struct {
    Name          string
    Born          int
    Roles         []string
    Skills        []string
    CurrentFocus  string
    Organization  Organization
    Pronouns      string
}

type Project struct {
    Name string
    Link string
}

type TechnicalSkills struct {
    Languages  []string
    Frameworks []string
    Tools      []string
}

func main() {
    about := AboutMe{
        Name:         "Nguyen Huynh Dang Nhut",
        Born:         2008,
        Roles:        []string{"High School Student", "Software Developer", "AI Enthusiast"},
        Skills:       []string{"Python", "OpenCV", "AI", "HTML", "JavaScript"},
        CurrentFocus: "AI Engineer",
        Organization: Organization{
            Name:      "CodliRo",
            Position:  "CGO & Founder",
            Projects:  []string{"Focumia", "Writedownia", "PrompTEA"},
            Teammates: []string{"@zakagjins", "@huynguyennhut"},
        },
        Pronouns: "He/Him",
    }

    story := `
Summer 2019: Started coding with Scratch → Built animations & games.
Learned Python + Arduino → Created LED blinkers, motor controllers, sensors.
Discovered AI (ML2019) → Trained my first model to recognize patterns.
Journey: Scratch → Python → Arduino → AI.
`

    projects := []Project{
        {"AZOTA BYPASS", "https://dangnhutnguyen.github.io/AZOTA-BYPASS-WEBSITE-CONTAINER-SHOW/"},
        {"Harmonic Motion Simulator", "https://dangnhutnguyen.github.io/HARMONIC-MOTION/"},
        {"Focumia Website", "https://codliro.github.io/Focumia/"},
        {"My Portfolio", "https://dangnhutnguyen.github.io/Portfolio/"},
    }

    skills := TechnicalSkills{
        Languages:  []string{"Python", "JavaScript", "HTML", "CSS", "C++", "Java", "Golang", "C#"},
        Frameworks: []string{"Flask", "React", "Django"},
        Tools:      []string{"Docker", "Git", "VS Code", "Nginx", "AWS", "Azure"},
    }

    fmt.Printf("=== ABOUT ME ===\nName: %s\nBorn: %d\nRoles: %s\n\n", 
        about.Name, about.Born, strings.Join(about.Roles, ", "))
    
    fmt.Printf("=== STORY ===\n%s\n", story)

    fmt.Println("=== PROJECTS ===")
    for _, p := range projects {
        fmt.Printf("- %s → %s\n", p.Name, p.Link)
    }

    fmt.Println("\n=== TECHNICAL SKILLS ===")
    fmt.Println("Languages :", strings.Join(skills.Languages, ", "))
    fmt.Println("Frameworks:", strings.Join(skills.Frameworks, ", "))
    fmt.Println("Tools     :", strings.Join(skills.Tools, ", "))
}
