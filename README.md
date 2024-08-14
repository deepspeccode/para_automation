import os

def create_para_structure(base_path):
    para_structure = {
        'Projects': [
            'Website Redesign',
            'Quarterly Report',
            'Home Renovation',
            'Learn Spanish',
            'Vacation Planning',
            'Product Launch',
            'Fitness Challenge',
            'Book Writing',
            'Charity Fundraiser',
            'Garden Makeover'
        ],
        'Areas': [
            'Health',
            'Finances',
            'Career',
            'Family',
            'Personal Development',
            'Home Management',
            'Relationships',
            'Hobbies',
            'Community Involvement',
            'Education'
        ],
        'Resources': [
            'Marketing',
            'Productivity',
            'Technology',
            'Cooking',
            'Travel',
            'Personal Finance',
            'Self-Improvement',
            'Design Inspiration',
            'Industry Trends',
            'Book Summaries'
        ],
        'Archive': [
            'Completed Projects',
            'Old Areas',
            'Outdated Resources',
            'Past Jobs',
            'Former Hobbies',
            'Completed Courses',
            'Past Events',
            'Old Versions',
            'Inactive Clients',
            'Discontinued Products'
        ]
    }
    
    for main_folder, subfolders in para_structure.items():
        main_folder_path = os.path.join(base_path, main_folder)
        os.makedirs(main_folder_path, exist_ok=True)
        print(f"Created main folder: {main_folder_path}")
        
        for subfolder in subfolders:
            subfolder_path = os.path.join(main_folder_path, subfolder)
            os.makedirs(subfolder_path, exist_ok=True)
            print(f"  Created subfolder: {subfolder_path}")
        
    print("PARA folder structure with extended subfolders created successfully!")

# Usage
base_path = input("Enter the base path where you want to create the PARA structure: ")
create_para_structure(base_path)
