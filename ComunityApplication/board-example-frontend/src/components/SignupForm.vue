<template>
    <form novalidate>
        <fieldset>
            <input type="text"
                    v-model="name"
                    placeholder="이름을 입력해주세요." />
            <input type="email"
                    v-model="email"
                    placeholder="이메일을 입력해주세요." />
            <input type="password"
                    v-model="password"
                    placeholder="비밀번호를 입력해주세요." />
            <input type="password"
                    v-model="passwordConfirm"
                    placeholder="비밀번호를 다시 한번 입력해주세요." />
            <button type="submit">회원가입</button>
        </fieldset>
    </form>
</template>

<script>
export default {
    name : 'SignupForm',
    data() {
        return {
            name : '',
            email : '',
            password : '',
            passwordConfirm: ''
        }
    }
}
</script>