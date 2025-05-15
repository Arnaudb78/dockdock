FROM node:20-alpine

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and pnpm-lock.yaml
COPY package.json pnpm-lock.yaml ./

# Install pnpm
RUN npm install -g pnpm

# Install dependencies
RUN pnpm install

# Copy application source
COPY . .

# Expose application port
EXPOSE 3000

# Start application in development mode
CMD ["sh", "-c", "pnpm run build && pnpm run start:prod"] 