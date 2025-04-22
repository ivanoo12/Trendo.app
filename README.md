# Trendo.app
import React from "react";

export default function ChatApp() {
  const countries = [
    { name: "العراق", flag: "🇮🇶", users: 1723, rooms: 111 },
    { name: "سورية", flag: "🇸🇾", users: 1004, rooms: 70 },
    { name: "السعودية", flag: "🇸🇦", users: 774, rooms: 35 },
    { name: "الأردن", flag: "🇯🇴", users: 643, rooms: 22 },
    { name: "لبنان", flag: "🇱🇧", users: 312, rooms: 18 },
    { name: "فلسطين", flag: "🇵🇸", users: 208, rooms: 21 },
  ];

  const rooms = [
    { name: "أحلى صداقه..أساطير الدردشه", users: 110 },
    { name: "جـواهـر الــدردشــة الأردنيــة", users: 106 },
    { name: "أخـوة أنـظـيـفـة", users: 98 },
    { name: "هـمـســآت الــنـعـمـة بــالـقـمـر", users: 88 },
    { name: "ملتقى الأحبة الغرفة العامة", users: 83 },
    { name: "ثاني سوريا.. ملتقى العزل", users: 73 },
    { name: "شات أهل سورياAL00oRdKhAlEd", users: 70 },
    { name: "أحلى لمة مصرية عربية", users: 67 },
  ];

  return (
    <div className="h-screen flex flex-col">
      {/* Header */}
      <div className="bg-gray-800 text-white px-4 py-2 text-xl font-bold">All2Chat</div>

      {/* Main Content */}
      <div className="flex flex-1">
        {/* Sidebar */}
        <div className="w-64 bg-gray-100 border-r p-2 overflow-y-auto">
          <h2 className="font-bold text-lg mb-2">الدول</h2>
          {countries.map((country, idx) => (
            <div
              key={idx}
              className="flex justify-between items-center mb-2 p-2 bg-white rounded shadow"
            >
              <div className="flex items-center gap-2">
                <span>{country.flag}</span>
                <span>{country.name}</span>
              </div>
              <div className="text-sm text-gray-500">{country.users} مستخدم</div>
            </div>
          ))}
        </div>

        {/* Chat Rooms List */}
        <div className="flex-1 p-4 overflow-y-auto">
          <h2 className="font-bold text-lg mb-4">الغرف المميزة</h2>
          {rooms.map((room, idx) => (
            <div
              key={idx}
              className="flex justify-between items-center p-3 mb-2 bg-blue-50 border-l-4 border-yellow-400 rounded shadow"
            >
              <span className="text-right w-full">⭐ {room.name}</span>
              <span className="text-gray-600 text-sm">{room.users}</span>
            </div>
          ))}
        </div>
      </div>

      {/* Footer Ads */}
      <div className="flex justify-around bg-purple-200 py-2 text-center text-sm">
        <div className="bg-pink-300 px-4 py-1 rounded">كوبون هوامير الخليج</div>
        <div className="bg-yellow-300 px-4 py-1 rounded">دندنه سعوديه كشيشينو</div>
        <div className="bg-purple-500 text-white px-4 py-1 rounded">السعودية أحلى الأوقات</div>
      </div>
    </div>
  );
}
