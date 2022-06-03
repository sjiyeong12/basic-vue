<template>
  <h1>form element Join</h1>
  <form action="Vue20_memberList.vue" ref="frm">
    <fieldset>
      <legend>회원 가입</legend>
      <div>
        <label for="id" class="title">ID</label>
        <input type="text" ref="id" id="id" />
      </div>
      <div>
        <label for="name" class="title">Name</label>
        <input type="text" ref="name" id="name" />
      </div>
      <div>
        <label for="pass" class="title">Password</label>
        <input type="password" ref="pass" id="pass" />
      </div>
      <div>
        <label class="title">RePassword</label>
        <input type="password" ref="repass" id="repass" />
      </div>
      <div class="divHobby">
        <label class="title">Hobby </label>
        <label :for="item" v-for="(item, i) in hobbyList" :key="i">
          {{item}}<input type="checkbox" name="hobby" id="item" :value="item" />
        </label>
      </div>
      <div class="divGender">
        <label class="title">Gender</label>
                <label :for="item" v-for="(item, i) in genderList" :key="i">
          {{item}}<input type="radio" name="gender" id="item" :ref="item" :value="item" v-model="hobby" />
        </label>
      </div>
      <div class="divMobile">
        <label for="id" class="title">Mobile</label>
        <select v-model="mobile" ref = "m1" id="mobile">
          <option :value="item" v-for="(item,i) in mobileList" :key="i">{{item}}</option>
        </select> - <input type="text" ref="m2" class="m"> -
         <input type="text" ref="m3" class="m">
        <input type="hidden" name="mobile" ref="mobile">
      </div>

      <div class="divBtn">
        <label class="title"></label>
        <button ref="btnJoin" @click="join" class="btn-margin">가입</button>
        <button ref="btnCancel" @click="cancel" class="btn-margin">취소</button>
      </div>
    </fieldset>
  </form>
</template>

<script>
export default {
  data: () => ({
    hobby: [""],
    hobbyList: ["축구", "배구", "농구"],
    gender:'여',
    genderList:['남','여'],
    mobile: '010',
    mobileList:['010','011','016'],
  }),
  methods:{
    join(){
      const frm = this.$refs.frm
      const id = this.$refs.id
      const name = this.$refs.name
      const pass = this.$refs.pass
      const repass = this.$refs.repass
      const m1 = this.$refs.m1
      const m2 = this.$refs.m2
      const m3 = this.$refs.m3
      // const mobile = this.$refs.mobile
       if (frm.value == "") {
            alert("폼을 입력하세요");
            frm.focus();
            return;
          }
       if (id.value == "") {
            alert("아이디를 입력하세요");
            id.focus();
            return;
          }
       if (pass.value == "") {
            alert("비밀번호를 입력하세요");
            pass.focus();
            return;
          }
      if (pass.value != repass.value) {
            alert("비밀번호가 맞지 않습니다");
            pass.value = "";
            repass.value = "";
            pass.focus();
            return;
          }
      if (name.value == "") {
        alert("이름을 입력하세요");
        name.focus();
        return;
      }
      if (m1.value == "") {
        alert("전화번호를 입력하세요");
        m1.focus();
        return;
      }
      if (m2.value == "") {
        alert("전화번호를 입력하세요");
        m2.focus();
        return;
      }
      if (m3.value == "") {
        alert("전화번호를 입력하세요");
        m3.focus();
        return;
      }

    },
    cancel(){
      const frm = this.$refs.frm
      const radioFemale = this.$refs.여
      frm.reset()
      radioFemale.checked = true
    }
  }
};
</script>

<style>
.title {
  display: inline-block;
  width: 120px;
  margin: 5px;
  text-align: left;
}
#mobile {height: 25px;} 

.m {width: 50px;}
.btn-margin {margin:20px 10px;}
.divHobby{
  position: relative;
  left: -10px
}
.divGender{
  position: relative;
  left: -51px
}
.divMobile{
  position: relative;
  left: 10px
}
.divBtn{
  position: relative;
  left: -36px
}
/* fieldset div {
  width: 300px;
  text-align: center;
} */
</style>