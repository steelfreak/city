## Entities and Attributes in a City Web Directory

A web directory for a city typically organizes a wide range of local information into structured entities, each with its own set of attributes. Below are the most common entities and their typical attributes found in such directories.

### Common Entities

- **Businesses**
- **Residents**
- **Educational Institutions**
- **Healthcare Facilities**
- **Government Offices**
- **Community Resources**
- **Events**
- **Points of Interest (Attractions, Parks, Museums)**
- **Utility Services**
- **Law Enforcement**
- **Non-Profit Organizations**

### Example Table: Entities and Their Attributes

| Entity                  | Typical Attributes                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------|
| Business                | Name, Category, Address, Phone, Email, Website, Hours, Description, Map Location, Reviews           |
| Resident                | Name, Address, Phone, Occupation (if included), Email                                               |
| Educational Institution | Name, Type (School, College), Address, Phone, Website, Description                                  |
| Healthcare Facility     | Name, Type (Hospital, Clinic), Address, Phone, Website, Services Offered                            |
| Government Office       | Name, Department, Address, Phone, Email, Website, Office Hours                                      |
| Community Resource      | Name, Type (Library, Center), Address, Phone, Website, Description                                  |
| Event                   | Name, Date, Time, Location, Description, Organizer, Registration Link                               |
| Point of Interest       | Name, Type (Park, Museum), Address, Description, Hours, Entry Fee                                   |
| Utility Service         | Name, Type (Water, Electricity), Address, Phone, Website, Emergency Contact                         |
| Law Enforcement         | Name, Address, Phone, Website, Jurisdiction                                                         |
| Non-Profit Organization | Name, Type, Address, Phone, Website, Mission, Services Provided                                     |

### Additional Features/Attributes

- **Categories and Subcategories:** Businesses and services are often grouped by type or industry for easier navigation[1][2].
- **Interactive Maps:** Many directories include geolocation data for mapping and directions[2].
- **User Reviews and Ratings:** For businesses and attractions, user-generated feedback is common[2].
- **Photos and Media:** Listings may include images or videos to enhance descriptions.
- **Search and Filtering Options:** Advanced search based on categories, location, or attributes[1][2].
- **Contact and Social Links:** Direct links to social media or contact forms.

### Typical Directory Structure

- **Homepage:** Featured categories, search bar, highlights of new or popular listings.
- **Category Pages:** Listings grouped by type (e.g., Restaurants, Schools).
- **Detail Pages:** Full information for each entity, including all attributes listed above[1][3].

### Summary

A city web directory is a comprehensive resource that centralizes information about local entities, each described by a set of attributes relevant to its type. The structure and depth of attributes can vary based on the directory’s purpose and audience, but the core goal is to make local information easily accessible and searchable for residents and visitors[1][2][4].

[1] https://wpgeodirectory.com/how-to-build-a-city-directory-in-wordpress/
[2] https://www.brilliantdirectories.com/blog/5-popular-city-directory-themes-for-local-travel-directories
[3] https://templatic.com/wp/create-city-directory-website-with-geoplaces/
[4] https://www.consumersearch.com/technology/create-successful-online-city-directory-community
[5] https://docs.secureauth.com/0902/en/active-directory-attributes-list.html
[6] https://opentextbc.ca/dbdesign01/chapter/chapter-8-entity-relationship-model/
[7] https://techdocs.broadcom.com/us/en/ca-mainframe-software/database-management/ca-idms/19-0/administrating/database-design/identifying-attributes/identifying-the-attributes-of-each-entity.html
[8] https://www.freeprojectz.com/entity-relationship/telephone-directory-management-system-er-diagram
[9] https://businessdirectoryplugin.com/how-to-build-a-city-directory-in-wordpress/
[10] https://opendata.stackexchange.com/questions/15385/wikidata-sparql-get-company-entities-and-the-location-of-their-headquarters
[11] https://www.gopeak.io/blog/directory-websites
[12] https://opendata.stackexchange.com/questions/422/is-there-a-list-database-or-api-that-contains-the-urls-for-united-states-city-a
[13] https://wbcomdesigns.com/types-of-web-directories/
[14] https://www.collaboard.app/en/blog/entity-relationship-model/
[15] https://www.edirectory.com/updates/how-to-create-a-directory-website/
[16] https://templatic.com/wordpress-directory-themes/city-guide/
[17] https://docs.devo.com/space/latest/1065844743/Using+entities+attributes+in+triggered+Alerts
[18] https://themeforest.net/search/city%20directory
[19] https://codecanyon.net/item/city-guide-directory-portal/15315828
[20] https://schema.org/City



City Web Directory – Responsive Design Demo
Below is a complete, attractive, and responsive HTML, CSS, and JavaScript demo for a city web directory. This example includes a homepage with a search bar, interactive category cards, and a modal dialog to display entity attributes. The design adapts smoothly to desktop and mobile screens.






```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>City Web Directory</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background: #f4f7f6;
            color: #333;
            line-height: 1.6;
            padding: 20px;
        }
        header {
            text-align: center;
            margin-bottom: 20px;
        }
        header h1 {
            color: #2c3e50;
            font-weight: 700;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        .search-bar {
            max-width: 600px;
            margin: 0 auto 30px auto;
            display: flex;
            border-radius: 30px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        .search-bar input {
            flex: 1;
            padding: 12px 20px;
            border: none;
            font-size: 1rem;
            outline: none;
        }
        .search-bar button {
            background: #3498db;
            border: none;
            color: white;
            padding: 12px 20px;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s ease;
        }
        .search-bar button:hover {
            background: #2980b9;
        }
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }
        .category-card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            padding: 20px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        .category-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }
        .category-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            color: #3498db;
        }
        .category-name {
            font-size: 1.25rem;
            font-weight: 700;
            color: #2c3e50;
        }
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: rgba(0,0,0,0.5);
            display: none;
            justify-content: center;
            align-items: center;
            padding: 20px;
            z-index: 1000;
        }
        .modal.active {
            display: flex;
        }
        .modal-content {
            background: white;
            border-radius: 12px;
            max-width: 600px;
            width: 100%;
            padding: 30px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.2);
            position: relative;
            overflow-y: auto;
            max-height: 80vh;
        }
        .modal-close {
            position: absolute;
            top: 15px;
            right: 15px;
            background: #e74c3c;
            border: none;
            color: white;
            font-size: 1.2rem;
            border-radius: 50%;
            width: 32px;
            height: 32px;
            cursor: pointer;
            font-weight: 700;
            line-height: 1;
        }
        .modal-close:hover {
            background: #c0392b;
        }
        .modal-content h2 {
            margin-bottom: 15px;
            color: #34495e;
        }
        .modal-content p {
            margin-bottom: 10px;
            font-size: 1rem;
            color: #555;
        }
        .modal-content .attribute-label {
            font-weight: 600;
            color: #2c3e50;
        }
        @media (max-width: 600px) {
            header h1 {
                font-size: 1.8rem;
            }
            .category-card {
                padding: 15px;
            }
            .category-icon {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>City Web Directory</h1>
        <div class="search-bar">
            <input type="text" id="searchInput" placeholder="Search categories or entities...">
            <button onclick="searchCategories()">Search</button>
        </div>
    </header>
    <main>
        <div class="categories" id="categoriesContainer">
            <!-- Category cards will be inserted here dynamically -->
        </div>
    </main>

    <div class="modal" id="detailModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">×</button>
            <h2 id="modalTitle">Category Name</h2>
            <div id="modalAttributes">
                <!-- Attributes will be shown here -->
            </div>
        </div>
    </div>

    <script>
        const categories = [
            { name: 'Businesses', icon: '🏢', attributes: ['Name', 'Category', 'Address', 'Phone', 'Email', 'Website', 'Hours', 'Description', 'Map Location', 'Reviews'] },
            { name: 'Residents', icon: '👤', attributes: ['Name', 'Address', 'Phone', 'Occupation', 'Email'] },
            { name: 'Educational Institutions', icon: '🎓', attributes: ['Name', 'Type', 'Address', 'Phone', 'Website', 'Description'] },
            { name: 'Healthcare Facilities', icon: '🏥', attributes: ['Name', 'Type', 'Address', 'Phone', 'Website', 'Services Offered'] },
            { name: 'Government Offices', icon: '🏛️', attributes: ['Name', 'Department', 'Address', 'Phone', 'Email', 'Website', 'Office Hours'] },
            { name: 'Community Resources', icon: '🏘️', attributes: ['Name', 'Type', 'Address', 'Phone', 'Website', 'Description'] },
            { name: 'Events', icon: '📅', attributes: ['Name', 'Date', 'Time', 'Location', 'Description', 'Organizer', 'Registration Link'] },
            { name: 'Points of Interest', icon: '📍', attributes: ['Name', 'Type', 'Address', 'Description', 'Hours', 'Entry Fee'] },
            { name: 'Utility Services', icon: '💡', attributes: ['Name', 'Type', 'Address', 'Phone', 'Website', 'Emergency Contact'] },
            { name: 'Law Enforcement', icon: '🚓', attributes: ['Name', 'Address', 'Phone', 'Website', 'Jurisdiction'] },
            { name: 'Non-Profit Organizations', icon: '🤝', attributes: ['Name', 'Type', 'Address', 'Phone', 'Website', 'Mission', 'Services Provided'] },
        ];

        const categoriesContainer = document.getElementById('categoriesContainer');
        const modal = document.getElementById('detailModal');
        const modalTitle = document.getElementById('modalTitle');
        const modalAttributes = document.getElementById('modalAttributes');

        function createCategoryCard(category) {
            const card = document.createElement('div');
            card.className = 'category-card';
            card.innerHTML = `
                <div class="category-icon">${category.icon}</div>
                <div class="category-name">${category.name}</div>
            `;
            card.addEventListener('click', () => showDetails(category));
            return card;
        }

        function showDetails(category) {
            modalTitle.textContent = category.name;
            modalAttributes.innerHTML = '';
            category.attributes.forEach(attr => {
                const p = document.createElement('p');
                p.innerHTML = `<span class="attribute-label">${attr}:</span> Example data for ${attr.toLowerCase()}.`;
                modalAttributes.appendChild(p);
            });
            modal.classList.add('active');
        }

        function closeModal() {
            modal.classList.remove('active');
        }

        function searchCategories() {
            const query = document.getElementById('searchInput').value.toLowerCase();
            categoriesContainer.innerHTML = '';
            const filtered = categories.filter(cat => cat.name.toLowerCase().includes(query));
            if (filtered.length === 0) {
                categoriesContainer.innerHTML = '<p style="text-align:center; color:#888;">No categories found.</p>';
                return;
            }
            filtered.forEach(cat => {
                categoriesContainer.appendChild(createCategoryCard(cat));
            });
        }

        // Initial load
        categories.forEach(cat => {
            categoriesContainer.appendChild(createCategoryCard(cat));
        });
    </script>
</body>
</html>


```
