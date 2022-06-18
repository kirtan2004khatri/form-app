<template>
    <div class="container border mt-5 w-25 p-5">
        <form>
            <div class="mb-3">
                <label for="exampleInputEmail1" class="form-label">Email address</label>
                <!-- Here you can use v-model:"variable name" to track change in it which are stored and tracked by a vairable -->
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp"
                    v-model="email">
                <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
            </div>
            <div class="mb-3">
                <label for="exampleInputPassword1" class="form-label">Password</label>
                <input type="password" class="form-control" id="exampleInputPassword1" v-model="pwd">
            </div>
            <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" id="exampleCheck1" v-model="check">
                <label class="form-check-label" for="exampleCheck1">Check me out</label>
            </div>
            <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" value="cooking" v-model="hobbies">Cooking
            </div>
              <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" value="dancing" v-model="hobbies">Dancing
            </div>
              <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" value="singing" v-model="hobbies">Singing
            </div>
              <div class="mb-3 form-check">
                <input type="checkbox" class="form-check-input" value="reading" v-model="hobbies">Reading
            </div>
            <div class="mb-3">
                <label for="disabledSelect" class="form-label">Role:</label>
                <select id="disabledSelect" class="form-select" v-model="role">
                    <option>Python</option>
                    <option>Java</option>
                    <option>JavaScript</option>
                    <option>C#</option>
                </select>
            </div>
            <div class="mb-3">
                <label for="skills" class="form-label">Skills</label>
                <input type="text" name="skills" class="form-control" v-model="tempSkills" @keyup="addSkills">
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
        </form>
    </div>
    <h1 class="text-center">{{ email }} and {{ pwd }} and {{role}} and check {{check}} and array {{hobbies}}</h1>
</template>

<script>
export default {
    name: "SignUpForm",
    data() {
        return {
            //These two variables are tracking the changes in form
            email: "123@gmail.com", pwd: "123456",role:"Python",check:false,hobbies:[],
            // By entering values in this tracking variables you are setting default values in form
            tempSkills:"",skills:[]
        }
    },
    method:{
        addSkills(e){
            console.log(e);
            console.log('hii')
        }
    }
}
</script>