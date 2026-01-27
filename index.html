<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <title>Smart Study Schedule</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- React -->
  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

  <!-- Babel (agar JSX bisa jalan di 1 file) -->
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f6f8;
      margin: 0;
      padding: 20px;
    }
    .container {
      max-width: 800px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
    }
    h1, h2 {
      color: #333;
    }
    button {
      margin-top: 5px;
      padding: 6px 10px;
      cursor: pointer;
    }
    ul {
      padding-left: 20px;
    }
    .box {
      border: 1px solid #ddd;
      padding: 10px;
      margin-bottom: 10px;
      border-radius: 6px;
    }
  </style>
</head>

<body>
  <div id="root"></div>

  <script type="text/babel">
    const { useState, useEffect } = React;

    function App() {
      const [schedule, setSchedule] = useState({
        Senin: [],
        Selasa: [],
        Rabu: [],
        Kamis: [],
        Jumat: [],
      });
      const [tasks, setTasks] = useState([]);
      const [notes, setNotes] = useState([]);

      // Load data
      useEffect(() => {
        setSchedule(JSON.parse(localStorage.getItem("schedule")) || schedule);
        setTasks(JSON.parse(localStorage.getItem("tasks")) || []);
        setNotes(JSON.parse(localStorage.getItem("notes")) || []);
      }, []);

      // Save data
      useEffect(() => {
        localStorage.setItem("schedule", JSON.stringify(schedule));
        localStorage.setItem("tasks", JSON.stringify(tasks));
        localStorage.setItem("notes", JSON.stringify(notes));
      }, [schedule, tasks, notes]);

      // Request notification permission
      useEffect(() => {
        if ("Notification" in window && Notification.permission === "default") {
          Notification.requestPermission();
        }
      }, []);

      // Notification checker
      useEffect(() => {
        const interval = setInterval(() => {
          const today = new Date().toISOString().split("T")[0];
          tasks.forEach(task => {
            if (task.date === today && !task.done) {
              if (Notification.permission === "granted") {
                new Notification("Pengingat Tugas / Ujian", {
                  body: task.title + " hari ini!",
                });
              }
            }
          });
        }, 60000);
        return () => clearInterval(interval);
      }, [tasks]);

      const addSubject = (day) => {
        const subject = prompt("Masukkan nama mata pelajaran:");
        if (!subject) return;
        setSchedule({ ...schedule, [day]: [...schedule[day], subject] });
      };

      const addTask = () => {
        const title = prompt("Nama tugas / ujian:");
        const date = prompt("Tanggal (YYYY-MM-DD):");
        if (!title || !date) return;
        setTasks([...tasks, { title, date, done: false }]);
      };

      const addNote = () => {
        const content = prompt("Tulis catatan belajar:");
        if (!content) return;
        setNotes([...notes, { content, date: new Date().toLocaleDateString() }]);
      };

      return (
        <div className="container">
          <h1>📚 Smart Study Schedule</h1>

          <h2>Jadwal Pelajaran</h2>
          {Object.keys(schedule).map(day => (
            <div className="box" key={day}>
              <b>{day}</b>
              <ul>
                {schedule[day].map((s, i) => <li key={i}>{s}</li>)}
              </ul>
              <button onClick={() => addSubject(day)}>Tambah Pelajaran</button>
            </div>
          ))}

          <h2>Pengingat Tugas & Ujian</h2>
          <button onClick={addTask}>Tambah Tugas / Ujian</button>
          <ul>
            {tasks.map((t, i) => (
              <li key={i}>{t.title} — {t.date}</li>
            ))}
          </ul>

          <h2>Catatan Belajar</h2>
          <button onClick={addNote}>Tambah Catatan</button>
          <ul>
            {notes.map((n, i) => (
              <li key={i}>{n.date}: {n.content}</li>
            ))}
          </ul>
        </div>
      );
    }

    ReactDOM.createRoot(document.getElementById("root")).render(<App />);
  </script>
</body>
</html>
