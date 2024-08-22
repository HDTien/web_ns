<template>
  <div class="main">
    <div class="page">
      <div class="page-header">
        <div class="page-title">Nhân viên</div>

        
         
        <div class="page-button">
          <button
            @click="btnAddOnClick"
            id="btn-add"
            class="btn btn-default btn-icon btn-icon--add-employee"
          >
            Thêm mới nhân viên
          </button>
        </div>
      </div>
      <div class="page-container">
        <div class="table">
          <div class="table-toolbar">
            <input
              type="text"
              class="input btn-icon btn-icon-search"
              placeholder="Tìm theo mã, tên nhân viên"
            />
            <button id="btn-reload" class="btn-reload"></button>
          </div>

          <div class="table-container">
            <table id="tbEmployeeList">
              <thead>
                <tr>
                  <th class="text-align-center" type="checkbox">
                    <input type="checkbox" />
                  </th>
                  <th class="text-align-left" model-name="employeeCode">
                    Mã nhân viên
                  </th>
                  <th class="text-align-left" model-name="fullName">
                    Tên nhân viên
                  </th>
                  <th class="text-align-left" model-name="genderName">
                    Giới tính
                  </th>
                  <th
                    class="text-align-left"
                    model-type="Date"
                    model-name="dateOfBirth"
                  >
                    Ngày sinh
                  </th>
                  <th class="text-align-left" model-name="identityNumber">
                    Số CMND
                  </th>
                  <th class="text-align-left" model-name="positionName">
                    Chức danh
                  </th>
                  <th class="text-align-left" model-name="departmentName">
                    Tên đơn vị
                  </th>
                  <th class="text-align-left" model-name="phoneNumber">
                    Số điện thoại
                  </th>
                  <th class="text-align-left" model-name="email">Email</th>
                  <th class="text-align-left" model-name="bankAccount">
                    Số Tài khoản
                  </th>
                  <th class="text-align-left" model-name="bankName">
                    Tên ngân hàng
                  </th>
                  <th class="text-align-left">Chức năng</th>
                </tr>
              </thead>
              <tbody>
                <tr v-show="isShowlistNv1">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV001</td>
                  <td class="text-align--left">Hoàng Đức Tiến</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hoàng Đức Tiến</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick1" id="btn-listnv1"> Ẩn </button>
                
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr v-show="isShowlistNv2">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV002</td>
                  <td class="text-align--left">Nguyễn Văn A</td>
                  <td class="text-align--left">Nguyễn Văn A</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick2" id="btn-listnv2"> Ẩn </button>
                   
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr v-show="isShowlistNv3">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV002</td>
                  <td class="text-align--left">Trần Văn B</td>
                  <td class="text-align--left">Trần Văn B</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick3" id="btn-listnv3"> Ẩn </button>
                    
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr  v-show="isShowlistNv4">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV003</td>
                  <td class="text-align--left">Tạ Văn C</td>
                  <td class="text-align--left">Tạ Văn C</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick4" id="btn-listnv4"> Ẩn </button>
                   
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>
                <tr  v-show="isShowlistNv5">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick5" id="btn-listnv5"> Ẩn </button>
                  
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>
                
                <tr  v-show="isShowlistNv6">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick6" id="btn-listnv6"> Ẩn </button>
                  
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr  v-show="isShowlistNv7">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick7" id="btn-listnv6"> Ẩn </button>
                  
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr  v-show="isShowlistNv8">
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button @click="btnAddOnClick8" id="btn-listnv6"> Ẩn </button>
                  
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>
                <tr  >
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button  id="btn-listnv6"> Ẩn </button>
                  
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                <tr >
                  <td class="text-align--left"><input type="checkbox" /></td>
                  <td class="text-align--left">NV004</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Tạ Văn D</td>
                  <td class="text-align--left">Nam</td>
                  <td class="text-align--center">2003-12-14</td>
                  <td class="text-align--left">0984771431</td>
                  <td class="text-align--left">Fresher</td>
                  <td class="text-align--left">MISA Software</td>
                  <td class="text-align--left">1111111111</td>
                  <td class="text-align--left">VC Bank</td>
                  <td class="text-align--left">Hà Nội</td>
                  <td class="text-align--left special">
                    <!-- <div class="fix">Sửa</div> -->
                    <button id="btn-listnv"> Ẩn </button>
                    
                    <div class="btn-table">
                    </div>
                  </td>
                </tr>

                

                <tr  v-for="(item, index) in employees" :key="index">
                  <td class="text-align-center"><input type="checkbox" /></td>
                  <td class="text-align-left">{{ item.employeeCode }}</td>
                  <td class="text-align-left">{{ item.fullName }}</td>
                  <td class="text-align-left">{{ item.gender }}</td>
                  <td class="text-align-left">{{ item.dateOfBirth }}</td>
                  <td class="text-align-left">{{ item.identityNumber }}</td>
                  <td class="text-align-left">{{ item.positionName }}</td>
                  <td class="text-align-left">{{ item.departmentName }}</td>
                  <td class="text-align-left">{{ item.phoneNumber }}</td>
                  <td class="text-align-left">{{ item.email }}</td>
                  <td class="text-align-left">{{ item.bankAccount }}</td>
                  <td class="text-align-left">{{ item.bankName }}</td>
                  <td class="text-align-center">
                    <div class="dropdown__text">Sửa</div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="table-paging">
            <div class="paging">
              <div class="paging-left">Tổng số: <b>10</b> bản ghi</div>
              <div class="paging-right">
                <div class="paging__pagesize">
                  <div class="pagesize-cbx">
                    <select name="" id="">
                      <option value="1" selected="selected">
                        10 bản ghi trên trang
                      </option>
                    </select>
                    <div class="pagesize-data" hidden>
                      <a class="pagesize-item pagesize-item--selected">
                        <div class="pagesize-item__text">10</div>
                        <div class="pagesize-item__icon"></div>
                      </a>
                      <a class="pagesize-item">
                        <div class="pagesize-item__text">20</div>
                        <div class="pagesize-item__icon"></div>
                      </a>
                      <a class="pagesize-item">
                        <div class="pagesize-item__text">50</div>
                        <div class="pagesize-item__icon"></div>
                      </a>
                      <a class="pagesize-item">
                        <div class="pagesize-item__text">100</div>
                        <div class="pagesize-item__icon"></div>
                      </a>
                    </div>
                  </div>
                  <div class="paging__index">
                    <p>Trước</p>
                    <div class="number-index">
                      <p>1</p>
                      <p>2</p>
                      <p>3</p>
                      <p>...</p>
                      <p>8</p>
                    </div>
                    <p>Sau</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <EmployeeDetail
    v-if="isShowPopup"
    :hideFunction="hidePopup"
    @hideMe="hidePopup"
  ></EmployeeDetail>
</template>

<script>
// import EmployeeDetail from '@/views/employee/EmployeeDetail.vue';
import EmployeeDetail from "@/views/employee/EmployeeDetail.vue";
export default {
  name: "TheMain",
  props: ["name"],
  components: { EmployeeDetail },
  created() {
    this.name;
    this.fullname;

    fetch("https://cukcuk.manhnv.net/api/v1/Employees")
      .then((res) => res.json())
      .then((data) => {
        console.log(data);
        this.employees = data;
      });
  },
  methods: {
    btnAddOnClick() {
      this.isShowPopup = true;
    },
    btnAddOnClick1(){
      this.isShowlistNv1 = false;
      
    },

    btnAddOnClick2(){
      this.isShowlistNv2 = false;
      
    },
    btnAddOnClick3(){
      this.isShowlistNv3 = false;
      
    },
    btnAddOnClick4(){
      this.isShowlistNv4 = false;
      
    },
    btnAddOnClick5(){
      this.isShowlistNv5 = false;
      
    },
    btnAddOnClick6(){
      this.isShowlistNv6 = false;
      
    },
    btnAddOnClick7(){
      this.isShowlistNv7 = false;
      
    },
    btnAddOnClick8(){
      this.isShowlistNv8 = false;
      
    },

    hidePopup() {
      this.isShowPopup = false;
    },
  },
  data() {
    return {
      employees: [],
      isShowPopup: false,
      isShowlistNv1: true,
      isShowlistNv2: true,
      isShowlistNv3: true,
      isShowlistNv4: true,
      
      isShowlistNv5: true,
      isShowlistNv6: true,
      isShowlistNv7: true,
      isShowlistNv8: true,
      isShowlistNv9: true,
      isShowlistNv10: true,
    };
  },
};
</script>

<style></style>
