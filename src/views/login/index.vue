<template>
	<div class="login-container">
		<el-form class="login-form">
			<h3 class="title">系统登录</h3>
			<el-form-item>
				<el-input prefix-icon="el-icon-user" placeholder="手机号"></el-input>
			</el-form-item>
			<el-form-item>
				<el-input prefix-icon="el-icon-lock" placeholder="验证码">
					<el-button type="primary" slot="append">获取验证码</el-button>
				</el-input>
			</el-form-item>
			<el-button class="login-handle" type="primary" @click="add">登录</el-button>
		</el-form>
	</div>
</template>

<script>
export default {
	name: 'Login',
	data() {
		return {
			msg: 1,
		}
	},
	methods: {
		add() {
			this.msg++
		},
	},
}
</script>

<style lang="less" scoped>
.login-form {
	width: 520px;
	margin: auto;
	padding: 140px 35px 0;

    .title {
        font-size: 26px;
        text-align: center;
    }

	/deep/ .el-input-group__append {
		color: #fff;
		background-color: #409eff;
	}

    .login-handle {
        width: 100%;
    }
}
</style>
