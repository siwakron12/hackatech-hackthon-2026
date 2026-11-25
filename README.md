
# MeetFan

**MeetFan** คือแพลตฟอร์มที่ช่วยให้คนที่มีความสนใจคล้ายกันได้เจอกันผ่าน "อีเวนต์" ในชีวิตจริง — ไม่ว่าจะเป็นงานออกกำลังกาย นิทรรศการศิลปะ หรือแฮกกาธอน ผู้ใช้สามารถค้นหาอีเวนต์ใกล้ตัว, ปัดเลือกคนที่อยากรู้จัก (คล้าย swipe การ์ด), จับคู่กันเมื่อสนใจตรงกัน แล้วเริ่มแชทได้ทันที

> 🏆 **โปรเจคนี้เป็นผลงานที่ชนะร่วม 3 ทีม (Winner)** จากกิจกรรมแฮกกาธอนที่จัดโดย **[CreativeLab TH](https://www.facebook.com/CreativeLabTH)**

<div style="display: flex; justify-content: space-between; align-items: flex-start; gap: 12px; flex-wrap: wrap;">
  <img width="485" height="956" alt="a" src="https://github.com/user-attachments/assets/77c4164d-f5da-456f-b3ee-918318036aeb" style="max-width: 48%; height: auto;" />
  <img width="483" height="953" alt="b" src="https://github.com/user-attachments/assets/4f1f476f-db66-4719-9149-7b519bd5a839" style="max-width: 48%; height: auto;" />
</div>

<img width="1536" height="2048" alt="721861453_866812636496352_7040138757786906049_n" src="https://github.com/user-attachments/assets/7b13b9f9-5382-4417-834c-5c61550c7b8d" />

---

## ✨ ฟีเจอร์หลัก

- **สำรวจอีเวนต์ใกล้ตัว** — แสดงอีเวนต์บนแผนที่ (Leaflet) พร้อมค้นหาและกรองตามความสนใจ
- **ระบบจับคู่ตามความสนใจ (Interest Matching)** — คำนวณคะแนนความเข้ากันระหว่างความสนใจของผู้ใช้กับแท็กของอีเวนต์
- **ปัดเพื่อจับคู่ (Swipe & Match)** — เข้าร่วมอีเวนต์แล้วปัดทำความรู้จักผู้เข้าร่วมคนอื่น เมื่อถูกใจกันทั้งสองฝ่ายจะเกิดแมตช์
- **แชทระหว่างคู่แมตช์** — พูดคุยกับคนที่แมตช์กันได้โดยตรงในแอป
- **โปรไฟล์ผู้ใช้** — ตั้งค่าอายุ เขต อาชีพ ความสนใจ และเป้าหมายในการเข้าร่วมกิจกรรม
- **ระบบสมัคร/เข้าสู่ระบบ** — ยืนยันตัวตนด้วย session และเข้ารหัสรหัสผ่านด้วย bcrypt
- **โอกาส/กิจกรรมแนะนำ (Opportunities)** — แนะนำอีเวนต์ที่เหมาะกับผู้ใช้แต่ละคน

## 🛠️ เทคโนโลยีที่ใช้

| ส่วนประกอบ | เทคโนโลยี |
|---|---|
| Framework | [Next.js 16](https://nextjs.org/) (App Router) + React 19 + TypeScript |
| Styling | Tailwind CSS 4 |
| ฐานข้อมูล / ORM | PostgreSQL + [Prisma](https://www.prisma.io/) |
| แผนที่ | Leaflet / React-Leaflet |
| ไอคอน | Lucide React |
| การยืนยันตัวตน | bcrypt + session-based auth |

## 📁 โครงสร้างโปรเจคโดยย่อ

```
src/
├── app/                 # หน้าเว็บและ API routes (App Router)
│   ├── (main)/          # หน้าแรก - สำรวจอีเวนต์ / แผนที่ / อีเวนต์ใกล้เคียง
│   ├── (Login)/         # หน้าล็อกอิน / สมัครสมาชิก
│   ├── chat/            # หน้าแชทของคู่แมตช์
│   ├── Event/            # รายละเอียดอีเวนต์
│   ├── opportunities/   # อีเวนต์/โอกาสแนะนำ
│   ├── profile/         # โปรไฟล์ผู้ใช้
│   └── api/             # REST API (auth, events, users, matches)
├── components/          # UI ที่ใช้ร่วมกัน (Bottom nav, Top bar, Auth provider)
├── services/            # Business logic (auth, event, match, interest-matching)
├── data/events/         # ข้อมูลอีเวนต์ตัวอย่างในรูปแบบ CSV
└── lib/                 # Prisma client, session helper, API response helper

prisma/
└── schema.prisma        # โมเดลข้อมูล: User, Event, EventParticipant, Swipe, Match, UserSession
```



## 🙏 ขอบคุณ

ขอบคุณ **[CreativeLab TH](https://www.facebook.com/CreativeLabTH)** ที่จัดกิจกรรมแฮกกาธอนดีๆ ให้ทีมได้เรียนรู้และสร้างสรรค์โปรเจคนี้ขึ้นมาจนคว้ารางวัลชนะร่วม 3 ทีม 🎉
<img width="1792" height="828" alt="758840577_907154665799494_6418498737433313954_n" src="https://github.com/user-attachments/assets/8f2e1863-0903-450b-84e3-6ac7cb9d3c85" />
