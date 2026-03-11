import React, { useMemo, useState } from "react";

export default function CalendarPage() {
  const monthNames = [
    "January", "February", "March", "April", "May", "June",
    "July", "August", "September", "October", "November", "December",
  ];

  const dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];

  const today = new Date();
  const [currentDate, setCurrentDate] = useState(
    new Date(today.getFullYear(), today.getMonth(), 1)
  );
  const [selectedDate, setSelectedDate] = useState(today);

  const year = currentDate.getFullYear();
  const month = currentDate.getMonth();
  const daysInMonth = new Date(year, month + 1, 0).getDate();
  const firstDay = new Date(year, month, 1).getDay();

  const calendarCells = useMemo(() => {
    const cells = [];
    const prevMonthDays = new Date(year, month, 0).getDate();

    for (let i = firstDay - 1; i >= 0; i -= 1) {
      cells.push({
        date: new Date(year, month - 1, prevMonthDays - i),
        isCurrentMonth: false,
      });
    }

    for (let day = 1; day <= daysInMonth; day += 1) {
      cells.push({
        date: new Date(year, month, day),
        isCurrentMonth: true,
      });
    }

    const remaining = 42 - cells.length;
    for (let day = 1; day <= remaining; day += 1) {
      cells.push({
        date: new Date(year, month + 1, day),
        isCurrentMonth: false,
      });
    }

    return cells;
  }, [year, month, daysInMonth, firstDay]);

  const isSameDate = (a, b) =>
    a.getFullYear() === b.getFullYear() &&
    a.getMonth() === b.getMonth() &&
    a.getDate() === b.getDate();

  const goToPreviousMonth = () => {
    setCurrentDate(new Date(year, month - 1, 1));
  };

  const goToNextMonth = () => {
    setCurrentDate(new Date(year, month + 1, 1));
  };

  const goToToday = () => {
    const now = new Date();
    setCurrentDate(new Date(now.getFullYear(), now.getMonth(), 1));
    setSelectedDate(now);
  };

  return (
    <div className="min-h-screen bg-slate-100 p-4 md:p-8">
      <div className="mx-auto max-w-5xl">
        <div className="overflow-hidden rounded-3xl bg-white shadow-xl ring-1 ring-slate-200">
          <div className="bg-gradient-to-r from-slate-900 to-slate-700 px-6 py-5 text-white">
            <div className="flex flex-col gap-4 md:flex-row md:items-center md:justify-between">
              <div>
                <h1 className="text-2xl font-bold tracking-tight md:text-3xl">Calendar</h1>
                <p className="mt-1 text-sm text-slate-200">
                  A clean monthly calendar with simple navigation
                </p>
              </div>
              <button
                onClick={goToToday}
                className="rounded-2xl bg-white/15 px-4 py-2 text-sm font-medium backdrop-blur transition hover:bg-white/25"
              >
                Today
              </button>
            </div>
          </div>

          <div className="grid grid-cols-1 lg:grid-cols-[1.4fr_0.8fr]">
            <div className="p-4 md:p-6">
              <div className="mb-4 flex items-center justify-between gap-3">
                <button
                  onClick={goToPreviousMonth}
                  className="rounded-2xl border border-slate-200 px-4 py-2 text-sm font-medium text-slate-700 transition hover:bg-slate-50"
                >
                  ← Prev
                </button>

                <div className="text-center">
                  <h2 className="text-xl font-semibold text-slate-900 md:text-2xl">
                    {monthNames[month]} {year}
                  </h2>
                </div>

                <button
                  onClick={goToNextMonth}
                  className="rounded-2xl border border-slate-200 px-4 py-2 text-sm font-medium text-slate-700 transition hover:bg-slate-50"
                >
                  Next →
                </button>
              </div>

              <div className="mb-2 grid grid-cols-7 gap-2">
                {dayNames.map((day) => (
                  <div
                    key={day}
                    className="py-3 text-center text-sm font-semibold text-slate-500"
                  >
                    {day}
                  </div>
                ))}
              </div>

              <div className="grid grid-cols-7 gap-2">
                {calendarCells.map(({ date, isCurrentMonth }, index) => {
                  const isToday = isSameDate(date, today);
                  const isSelected = isSameDate(date, selectedDate);

                  return (
                    <button
                      key={`${date.toISOString()}-${index}`}
                      onClick={() => {
                        setSelectedDate(date);
                        setCurrentDate(new Date(date.getFullYear(), date.getMonth(), 1));
                      }}
                      className={[
                        "aspect-square rounded-2xl border p-2 text-left transition",
                        isCurrentMonth
                          ? "border-slate-200 bg-white hover:bg-slate-50"
                          : "border-slate-100 bg-slate-50 text-slate-400 hover:bg-slate-100",
                        isSelected ? "ring-2 ring-slate-900" : "",
                        isToday ? "border-blue-300 bg-blue-50" : "",
                      ].join(" ")}
                    >
                      <div className="flex h-full flex-col justify-between">
                        <span
                          className={[
                            "text-sm font-semibold",
                            isCurrentMonth ? "text-slate-800" : "text-slate-400",
                          ].join(" ")}
                        >
                          {date.getDate()}
                        </span>
                        {isToday && (
                          <span className="self-start rounded-full bg-blue-600 px-2 py-0.5 text-[10px] font-bold text-white">
                            TODAY
                          </span>
                        )}
                      </div>
                    </button>
                  );
                })}
              </div>
            </div>

            <div className="border-t border-slate-200 bg-slate-50 p-6 lg:border-l lg:border-t-0">
              <div className="sticky top-6">
                <p className="text-sm font-medium uppercase tracking-[0.2em] text-slate-400">
                  Selected Date
                </p>
                <h3 className="mt-2 text-2xl font-bold text-slate-900">
                  {selectedDate.toLocaleDateString("en-US", {
                    year: "numeric",
                    month: "long",
                    day: "numeric",
                    weekday: "long",
                  })}
                </h3>

                <div className="mt-6 rounded-3xl bg-white p-5 shadow-sm ring-1 ring-slate-200">
                  <p className="text-sm text-slate-500">Notes</p>
                  <p className="mt-2 text-sm leading-6 text-slate-700">
                    This is a simple calendar UI. You can extend it with schedules,
                    reminders, holiday data, or event storage.
                  </p>
                </div>

                <div className="mt-4 rounded-3xl bg-slate-900 p-5 text-white shadow-sm">
                  <p className="text-sm text-slate-300">Ideas to extend</p>
                  <ul className="mt-3 list-inside list-disc space-y-2 text-sm text-slate-100">
                    <li>Add event creation and editing</li>
                    <li>Connect to Google Calendar API</li>
                    <li>Show Korean public holidays</li>
                    <li>Add week and day views</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}
