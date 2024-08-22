<template>
         <div id="frmDetail" class="popup"  >
        <div  class="popup-form">
            <button class="popup__button" @click="btnCloseOnClick"></button>            
            <div class="popup__header">Thông tin nhân viên</div>
            <div class="popup__body">
                <div class="employee-info">
                    <div class="form-group general-info-left">
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeeCode">Mã <span class="required">*</span></label>
                                <input  oninput="" id="txtEmployeeCode" required class="input--required" type="text" value="" style="width: 100px;" @blur="validateEmployee">
                                <div class="error-info" id="error-info" hidden style="width: 100px;">
                                    Mã nhân viên không được phép trống
                                </div>
                            </div>
                            <div class="input-wrapper">
                                <label for="txtEmployeeName">Tên <span class="required">*</span></label>
                                <input id="txtEmployeeName" name required class="input--required" type="text" value="">
                                <div class="error-info" hidden>
                                    Tên không hợp lệ
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeeDV">Đơn vị <span class="required">*</span></label>
                                <input id="txtEmployeeDV" required class="input--required" type="text" value="">
                                <div class="error-info" hidden>
                                    Đơn vị không được phép trống
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeeCD">Chức danh</label>
                                <input id="txtEmployeeCD" class="input--required" type="text" value="">
                            </div>
                        </div>
                    </div>
                    <div class="form-group general-info-right">
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper" style="width: 150px;">
                                <label for="txtEmployeeBirthDate">Ngày sinh <span class="required">*</span></label>
                                <input id="txtEmployeeBirthDate" date class="input__datepicker input--required" type="date" value="">
                                <div class="error-date" hidden>
                                    Ngày sinh không hợp lệ
                                </div>
                                <div class="error-info" hidden>
                                    Ngày sinh không được phép trống
                                </div>
                            </div>
                            <div class="input-wrapper">
                                <label for="txtEmployeeGender">Giới tính <span class="required">*</span></label>
                                <div class="radio" id="txtEmployeeGender" required>
                                    <div class="test-radiobutton">
                                        <input type="radio" name="gt" class="radio-1">
                                        <span class="checkmark"></span>
                                        <label for="radio-1" class="radio-label">Nam</label>
                                    </div>
                                    <div class="test-radiobutton">
                                        <input type="radio" name="gt" class="radio-2">
                                        <span class="checkmark"></span>
                                        <label for="radio-2" class="radio-label">Nữ</label>
                                    </div>
                                    <div class="test-radiobutton">
                                        <input type="radio" name="gt" class="radio-3">
                                        <span class="checkmark"></span>
                                        <label for="radio-2" class="radio-label">Khác</label>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeeCMTND" title="Số chứng minh thư nhân dân">Số CMTND <span class="required">*</span></label>
                                <input id="txtEmployeeCMTND" idnumber required class="input--required" type="text" value="" style="width: 100%;">
                                <div class="error-info" hidden>
                                    Số CMND không hợp lệ
                                </div>
                            </div>
                            <div class="input-wrapper">
                                <label for="txtEmployeeDayCMT">Ngày cấp  <span class="required">*</span></label>
                                <input id="txtEmployeeDayCMT" date type="date" value="">
                                <div class="error-date" hidden>
                                    Ngày cấp không hợp lệ
                                </div>
                                <div class="error-info" hidden>
                                    Ngày sinh không được phép trống
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeeDayCMT">Nơi cấp</label>
                                <input id="txtEmployeeDayCMT" type="text" value="">
                            </div>
                        </div>
                    </div>
                    <div class="form-group contact-info">
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper" style="width: 100%;">
                                <label for="txtEmployeeAddress">Địa chỉ  <span class="required">*</span></label>
                                <input id="txtEmployeeAddress" required type="text" value="" >
                                <div class="error-info" hidden>
                                    Địa chỉ không được để trống
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                <label for="txtEmployeePhoneDD" title="Số điện thoại di động">Số ĐT di động <span class="required">*</span></label>
                                <input id="txtEmployeePhoneDD" required number type="text" value="">
                                <div class="error-info" hidden>
                                    Số điện thoại không hợp lệ
                                </div>
                            </div>

                            <div class="input-wrapper">
                                <label for="txtEmployeePhoneCD" title="Số điện thoại cố định">Số ĐT cố định</label>
                                <input id="txtEmployeePhoneCD" number type="text" value="" >
                                <div class="error-info" hidden>
                                    Số điện thoại không hợp lệ
                                </div>
                            </div>
                            <div class="input-wrapper">
                                <label for="txtEmployeeEmail">Email</label>
                                <input id="txtEmployeeEmail" required email type="text" value="" >
                                <div class="error-info" hidden>
                                    Email không hợp lệ
                                </div>
                            </div>
                        </div>
                        <div class="m-row m-flex m-col-gap-8">
                            <div class="input-wrapper">
                                    <label for="txtEmployeeBankNum">Tài khoản ngân hàng</label>
                                    <input id="txtEmployeeBankNum" nnum type="text" value="">
                                    <div class="error-info" hidden>
                                        Số tài khoản không hợp lệ
                                    </div>
                            </div>
                             <div class="input-wrapper">
                                    <label for="txtEmployeeBankName">Tên ngân hàng</label>
                                    <input id="txtEmployeeBankName" type="text" value="" >
                             </div>
                            <div class="input-wrapper">
                                    <label for="txtEmployeeBankBranch">Chi nhánh</label>
                                    <input id="txtEmployeeBankBranch" type="text" value="" >
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="popup__footer">
                <div class="popup-footer__left">
                    <button  @click="btnCloseOnClick"  id="btnCancel" class="btn btn--defaultwhite">Hủy</button>
                </div>
                <div class="popup-footer__right">
                    <button class="btn btn--defaultwhite" style="margin-right: 8px">Cất</button>
                    <button class="btn btn--default">Thêm mới</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
    name :"EmployeeDetail",
    props:["hideFunction"],
 
    methods: {
        btnCloseOnClick(){
        // this.hideFunction();
            this.$emit("hideMe");
        },

        validateEmployee(){
            var validValue = event.currentTarget.value;
            if(!validValue){
                event.currentTarget.classList.add("input--error");
                
                
            }else{
                event.currentTarget.classList.remove("input--error");         
            }
        },
    }

    
}
</script>
<style scoped>

</style>