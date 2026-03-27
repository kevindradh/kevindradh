using System;
using System.Collections.Generic;
using System.Threading.Tasks;

namespace GitHubProfile
{
    /// <summary>
    /// Hello World! Welcome to my GitHub.
    /// </summary>
    public class DeveloperProfile
    {
        // ==========================================
        // Basic Info
        // ==========================================
        public string Name { get; } = "Kevind Radhitya";
        public string Role { get; } = "Android Developer";
        public string Location { get; } = "Bondowoso, East Java, Indonesia";
        
        // ==========================================
        // Tech Stack & Skills
        // ==========================================
        public List<string> Skills { get; } = new List<string>
        {
            "C#", ".NET Core", "ASP.NET Web API", 
            "Entity Framework", "SQL Server", "Git", "Kotlin"
        };

        // ==========================================
        // Current Status
        // ==========================================
        public Dictionary<string, string> GetCurrentStatus()
        {
            return new Dictionary<string, string>
            {
                { "Learning", "Android Jetpack Compose" },
                { "School On", "SMKN 1 Bondowoso" }
            };
        }

        // ==========================================
        // Let's Connect!
        // ==========================================
        public async Task ContactMeAsync()
        {
            var links = new Dictionary<string, string>
            {
                { "Email", "radhityakevind@gmail.com" },
                { "Instagram", "kevind_radhitya" },
                { "Portfolio", "mepinn.my.id" }
            };

            foreach (var link in links)
            {
                Console.WriteLine($"{link.Key}: {link.Value}");
            }
            
            await Task.CompletedTask;
        }
    }
}
