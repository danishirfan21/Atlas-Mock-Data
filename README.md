# Atlas Mock Data API

Mock JSON data for the Atlas Knowledge Management System.

## 📦 Available Endpoints

Base URL: `https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/`

### Documents
- **All Documents**: `documents.json`
- **Example**: https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/documents.json

### Collections
- **All Collections**: `collections.json`
- **Example**: https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/collections.json

### Activities
- **Activity Feed**: `activities.json`
- **Example**: https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/activities.json

### Users
- **All Users**: `users.json`
- **Example**: https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/users.json

## 🔧 Usage

### Fetch with JavaScript
```javascript
const response = await fetch('https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/documents.json');
const documents = await response.json();
```

### Fetch with Next.js API Route
```typescript
// src/app/api/documents/route.ts
export async function GET() {
  const res = await fetch('https://raw.githubusercontent.com/danishirfan21/atlas-mock-data/main/data/documents.json');
  const data = await res.json();
  return Response.json(data);
}
```

## 📊 Data Schema

### Document
- `id` (number) - Unique identifier
- `title` (string) - Document title
- `snippet` (string) - Preview text (~60 chars)
- `body` (string) - Full HTML content
- `author` (string) - Author name
- `authorInitials` (string) - 2-letter initials
- `updatedAt` (string) - ISO date
- `status` (string) - "Published" | "Draft" | "In Review"
- `views` (number) - View count

### Collection
- `id` (number) - Unique identifier
- `name` (string) - Collection name
- `description` (string) - Description
- `icon` (string) - Emoji icon
- `iconBg` (string) - CSS gradient
- `documentCount` (number) - Number of docs
- `contributorCount` (number) - Number of contributors
- `createdAt` (string) - ISO date
- `updatedAt` (string) - ISO date

### Activity
- `id` (number) - Unique identifier
- `action` (string) - "created" | "updated" | "published" | "commented"
- `author` (string) - Author name
- `authorInitials` (string) - 2-letter initials
- `documentTitle` (string) - Related document
- `documentId` (number) - Document ID
- `timestamp` (string) - ISO date

## 📝 License

MIT - Free to use for development and testing

## 🔗 Related

- [Atlas Next.js App](https://github.com/danishirfan21/Atlas-Next)