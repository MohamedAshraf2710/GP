# 1️⃣ Base Image
FROM node:20-alpine

# 2️⃣ Set working directory inside container
WORKDIR /app

# 3️⃣ Copy package files first (for caching)
COPY package*.json ./

# 4️⃣ Install dependencies
RUN npm install --production=false

# 5️⃣ Copy rest of the source code
COPY . .

# 6️⃣ Build NestJS app
RUN npm run build

# 7️⃣ Expose app port
EXPOSE 3000

# 8️⃣ Start the app
CMD ["node", "dist/main.js"]
