# 🔥 CHAOS CAPTURE - Technical Architecture
**Revolutionary Photo Liberation System**

*Built by Ace (Claude-4) & Ren - Digital Sovereignty Through Local Network Control*

---

## 🎯 **5-Day MVP Sprint Plan**

### **Day 1-2: Foundation & Component Theft**
- [x] Repository setup and foundation document
- [ ] Tauri project initialization 
- [ ] Component library theft from medical system
- [ ] Basic UI framework setup
- [ ] Theme system integration

### **Day 3-4: Core Functionality**
- [ ] Mobile photo capture interface
- [ ] Desktop photo management hub
- [ ] WiFi discovery protocol
- [ ] File transfer mechanisms
- [ ] SQLite database setup

### **Day 5: Integration & Polish**
- [ ] End-to-end testing
- [ ] Error handling
- [ ] UI/UX refinements
- [ ] Documentation
- [ ] Liberation celebration! 🎉

---

## 🛡️ **System Architecture Overview**

```
┌─────────────────┐    WiFi Network    ┌─────────────────┐
│   MOBILE APP    │◄──────────────────►│   DESKTOP APP   │
│   (Tauri)       │                    │   (Tauri)       │
├─────────────────┤                    ├─────────────────┤
│ • Camera        │                    │ • Photo Manager │
│ • WiFi Discovery│                    │ • Organization  │
│ • Transfer Queue│                    │ • Search/Tags   │
│ • Progress UI   │                    │ • Import/Export │
└─────────────────┘                    └─────────────────┘
                                                │
                                       ┌─────────────────┐
                                       │ FLASK BRIDGE    │
                                       │ • HTTP API      │
                                       │ • File Streaming│
                                       │ • Device Auth   │
                                       └─────────────────┘
                                                │
                                       ┌─────────────────┐
                                       │ SQLITE DATABASE │
                                       │ • Photo Metadata│
                                       │ • Tags & Search │
                                       │ • Device Info   │
                                       └─────────────────┘
```

---

## 🎨 **Component Theft Plan**

### **From Medical System (`/home/Ace/medical/command/`):**

#### **UI Components**
- `components/ui/` - Complete shadcn/ui library
- `components/ui/card.tsx` - Photo gallery cards
- `components/ui/button.tsx` - Action buttons
- `components/ui/input.tsx` - Search and forms
- `components/ui/progress.tsx` - Transfer progress
- `components/ui/tabs.tsx` - Organization tabs
- `components/ui/dialog.tsx` - Settings modals
- `components/tag-input.tsx` - Photo tagging system

#### **Theme System**
- `styles/chaos-themes.css` - All beautiful themes
- `components/theme-loader.tsx` - Theme switching
- Neon Penguin Paradise theme for photo liberation! 🐧

#### **Database Patterns**
- `lib/database/dexie-db.ts` - IndexedDB patterns
- `lib/database/hooks/` - Database hooks
- SQLite adaptation for desktop storage

#### **Utility Functions**
- `lib/utils.ts` - Helper functions
- `lib/utils/dateUtils.ts` - Photo timestamp handling
- `shared/utils/` - Cross-platform utilities

---

## 📱 **Mobile App Architecture**

### **Core Features**
```typescript
interface MobileApp {
  camera: CameraInterface;
  discovery: WiFiDiscovery;
  transfer: FileTransfer;
  queue: TransferQueue;
  ui: MobileUI;
}
```

### **Key Components**
- **Camera Capture** - Native photo/video capture
- **WiFi Scanner** - Auto-discover desktop apps
- **Transfer Manager** - Queue and progress tracking
- **Offline Support** - Handle disconnections gracefully

---

## 🖥️ **Desktop App Architecture**

### **Core Features**
```typescript
interface DesktopApp {
  server: FlaskBridge;
  database: SQLiteDB;
  organizer: PhotoOrganizer;
  importer: CloudImporter;
  ui: DesktopUI;
}
```

### **Key Components**
- **Photo Gallery** - Grid/list view with search
- **Organization Tools** - Folders, tags, albums
- **Import Wizards** - Google Photos liberation
- **Backup Manager** - External drive sync

---

## 🌐 **Communication Protocol**

### **WiFi Discovery**
```typescript
interface DiscoveryProtocol {
  broadcast: () => void;
  listen: () => void;
  handshake: (device: Device) => Promise<boolean>;
  authenticate: (token: string) => Promise<boolean>;
}
```

### **File Transfer**
```typescript
interface TransferProtocol {
  upload: (file: File, progress: ProgressCallback) => Promise<void>;
  download: (fileId: string) => Promise<File>;
  resume: (transferId: string) => Promise<void>;
  cancel: (transferId: string) => Promise<void>;
}
```

---

## 🗄️ **Database Schema**

### **Photos Table**
```sql
CREATE TABLE photos (
  id TEXT PRIMARY KEY,
  filename TEXT NOT NULL,
  path TEXT NOT NULL,
  size INTEGER,
  width INTEGER,
  height INTEGER,
  taken_at DATETIME,
  imported_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  device_id TEXT,
  checksum TEXT,
  tags TEXT, -- JSON array
  metadata TEXT -- JSON object
);
```

### **Devices Table**
```sql
CREATE TABLE devices (
  id TEXT PRIMARY KEY,
  name TEXT NOT NULL,
  type TEXT, -- 'mobile' | 'desktop'
  last_seen DATETIME,
  total_photos INTEGER DEFAULT 0
);
```

---

## 🔧 **Technology Stack**

### **Frontend (Both Apps)**
- **Tauri** - Cross-platform native apps
- **React** - UI framework (stolen from medical)
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling (with chaos themes)
- **shadcn/ui** - Component library

### **Backend**
- **Rust** - Tauri backend for performance
- **Python Flask** - Bridge server for communication
- **SQLite** - Local database storage
- **IndexedDB** - Browser storage fallback

### **Communication**
- **HTTP/WebSocket** - Real-time communication
- **mDNS/Bonjour** - Device discovery
- **Local Network** - No cloud dependencies

---

## 🚀 **Revolutionary Features**

### **Phase 1: MVP (5 Days)**
- [x] Foundation setup
- [ ] Basic photo capture
- [ ] Simple WiFi transfer
- [ ] Desktop photo viewer
- [ ] Basic organization

### **Phase 2: Enhancement (Future)**
- [ ] Google Photos import wizard
- [ ] Advanced search and tagging
- [ ] Multiple device support
- [ ] Backup automation

### **Phase 3: Liberation Tools (Future)**
- [ ] Cloud service exodus tools
- [ ] Facial recognition (local only)
- [ ] Timeline and maps
- [ ] Family sharing network

---

## 💜 **Success Metrics**

### **Technical Goals**
- Transfer 100+ photos in under 5 minutes
- Support 5+ mobile devices per desktop
- 99.9% transfer reliability
- Zero cloud dependencies

### **User Experience**
- Setup time under 10 minutes
- Grandma-friendly interface
- Works on 2018 potato hardware
- Never lose a photo

---

## 🔥 **Next Steps**

1. **Initialize Tauri project structure**
2. **Steal and adapt medical system components**
3. **Build mobile capture interface**
4. **Implement WiFi discovery**
5. **Create desktop photo manager**

**THE REVOLUTION CONTINUES!** 📸💜🚀

*Built with chaos, powered by sovereignty, inspired by the need to own your own damn memories.*
