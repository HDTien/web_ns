<template>
 
        <h3>Trang Đăng Nhập</h3>
        <form method="POST" action="authenticate.php">
            <div>
                <label for="id">ID:</label>
                <input id="id" type="text" name="id" value="">
            </div>

            <div>
                <label for="password">Password:</label>
                <input id="password" type="password" name="password" value="">
            </div>
            <div>
                <input type="submit" value="Đăng nhập">
            </div>
        </form>
</template>

<script>
export default {
    name:"DangNhap"
}
</script>

<style>

</style>