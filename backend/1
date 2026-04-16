const express = require("express");
const dotenv = require("dotenv");
const connectDB = require("./config/db");

dotenv.config();
connectDB();

const app = express();
app.use(express.json());

// ✅ Root route
app.get("/", (req, res) => {
  res.send("API is running 🚀");
});

app.use("/api/users", require("./routes/userRoutes"));

app.listen(5000, "0.0.0.0", () => {
  console.log("Server running on port 5000");
});
