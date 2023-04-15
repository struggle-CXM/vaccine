<template>
  <div>
    <el-row>
      <el-col :span="12">
        <h1>{{ fullName }}</h1>
        <h2>{{ profession }}</h2>
        <p>{{ aboutMe }}</p>
      </el-col>
      <el-col :span="12">
        <img :src="profilePictureUrl" />
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <h3>My Skills</h3>
        <ul>
          <li v-for="(skill, index) in skills" :key="index">{{ skill }}</li>
        </ul>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <h3>Contact Me</h3>
        <ul>
          <li>
            <a :href="'mailto:' + email">{{ email }}</a>
          </li>
          <li>
            <a :href="'tel:' + phoneNumber">{{ phoneNumber }}</a>
          </li>
          <li>
            <a :href="github">{{ github }}</a>
          </li>
        </ul>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: "Your Name",
      profession: "Your Profession",
      aboutMe: "About Me",
      skills: ["Skill 1", "Skill 2", "Skill 3"],
      email: "youremail@example.com",
      phoneNumber: "123-456-7890",
      github: "https://github.com/yourusername",
      profilePictureUrl: "https://via.placeholder.com/400x400",
    };
  },
};
</script>
