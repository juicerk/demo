<!-- 错误示例：没有 key，切换时输入框内容会保留 -->
 <template>
    <button @click="login">login</button>
    <button @click="logout">logout</button>
    <!-- <template v-if="isLogin">
        <label>用户名1</label>
        <input v-model="username" placeholder="请输入用户名">
    </template>
    <template v-else>
        <label>用户名2</label>
        <input v-model="username" placeholder="请输入邮箱">
    </template> -->

    <p>添加 key 后，切换时输入框内容不会保留</p>
    <template v-if="isLogin">
        <label>用户名1</label>
        <input v-model="username" key="username1" placeholder="请输入用户名">
    </template>
    <template v-else>
        <label>用户名2</label>
        <input v-model="username" key="username2" placeholder="请输入邮箱">
    </template>
</template>

<script setup>
import { ref } from 'vue';

const username = ref('');
const email = ref('');

const isLogin = ref(false);

const login = function() {
    isLogin.value = true;
}

const logout = function() {
    isLogin.value = false;
}
</script>