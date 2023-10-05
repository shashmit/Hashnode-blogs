---
title: "Vite on Docker"
datePublished: Thu Oct 05 2023 23:14:42 GMT+0000 (Coordinated Universal Time)
cuid: clndsopxa000909kz4zf36qm2
slug: vite-on-docker
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696547622453/fde520ff-310b-4cd0-9ece-7b99dee00f55.png
tags: docker, bash, developer, reactjs, vite

---

I don't know how many of you guys have faced this or you will ever face it.

Bringing you this because when I was setting up my docker with Vite. I faced something that combined a lot of tweaking.

Let's just start with the basic setup first:

prerequisite:

* Docker
    
* Vite
    
* computer
    

STEP 1: Configure the Vite.config:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696546904296/1601d92a-0e04-4ea7-a30f-4be5a49ca6b9.png align="center")

```javascript
export default defineConfig({
  plugins: [react()],
  server: {
    host: true,
    port: 8000, // This is the port which we will use in docker
    // add the next lines if you're using windows and hot reload doesn't work
    watch: {
      usePolling: true,
    },
  },
});
```

In this whole configuration, the most important thing is PORT where you want to host the running client. So, you can put any PORT you want.

STEP 2: Now time for Dockerfile:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696547102928/24b85745-aa87-475b-bdb2-9910a24af5f3.png align="center")

In this bracket you have to just look into CMD as vite starts with Dev, I have set it to Dev. If you are using base react then start.

```dockerfile
FROM node:18.18.0-alpine

WORKDIR /code 
COPY package.json /code 
COPY package-lock.json /code 
RUN npm install 
COPY . .
CMD ["npm","run","dev"]
```

STEP 3: Lets compose it:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696547295033/4db846df-1248-4fb5-a454-586dde3b7abd.png align="center")

Final Step:

Here we use that port number we established before, the screenshot is of different activity. Hence for better understanding. Read the Code

```bash
docker run --rm -it --name web -p 8000:8000 react-docker:1.0.0-dev
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696547322301/1d8577eb-52ed-4694-b135-b1d0dc0ba970.png align="center")

WIth this you will be able to run your VITE in a container and later just host the image.

Hope you have learned something. And this might have helped you in your development.  
Like it | Share it

Feel free to hit me up on [Twitter](https://twitter.com/Shaashmit) or connect with me on [LinkedIn](https://www.linkedin.com/in/shashmit-kumar-23b75620a/) if you like this.