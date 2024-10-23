<template>
  <div class="main-card">
    <div class="tabs">
      <button class="tab active">Edit Profile</button>
      <button class="tab">Preferences</button>
      <button class="tab">Security</button>
    </div>
    <div class="user-info">
      <div class="avatar">
        <img src="../public/assets/images/avatar.png" alt="User Avatar" />
        <button class="pencil">
          <svg
            width="15.000000"
            height="15.000000"
            viewBox="0 0 15 15"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
          >
            <defs>
              <clipPath id="clip20_740">
                <rect
                  id="pencil-alt 1"
                  rx="-0.500000"
                  width="14.000000"
                  height="14.000000"
                  transform="translate(0.500000 0.500000)"
                  fill="white"
                  fill-opacity="0"
                />
              </clipPath>
            </defs>
            <rect
              id="pencil-alt 1"
              rx="-0.500000"
              width="14.000000"
              height="14.000000"
              transform="translate(0.500000 0.500000)"
              fill="#FFFFFF"
              fill-opacity="0"
            />
            <g clip-path="url(#clip20_740)">
              <path
                id="Vector"
                d="M14.58 4.16L13.23 5.51C13.09 5.65 12.87 5.65 12.73 5.51L9.48 2.26C9.34 2.12 9.34 1.9 9.48 1.76L10.83 0.41C11.38 -0.14 12.27 -0.14 12.82 0.41L14.58 2.17C15.13 2.72 15.13 3.61 14.58 4.16ZM8.32 2.92L0.63 10.61L0.01 14.17C-0.08 14.65 0.34 15.07 0.82 14.99L4.38 14.36L12.07 6.67C12.21 6.53 12.21 6.31 12.07 6.17L8.82 2.92C8.68 2.78 8.46 2.78 8.32 2.92ZM3.63 9.95C3.47 9.79 3.47 9.53 3.63 9.37L8.14 4.86C8.3 4.7 8.56 4.7 8.72 4.86C8.88 5.02 8.88 5.28 8.72 5.44L4.21 9.95C4.05 10.11 3.79 10.11 3.63 9.95ZM2.57 12.42L3.98 12.42L3.98 13.48L2.09 13.81L1.18 12.9L1.51 11.01L2.57 11.01L2.57 12.42Z"
                fill="#FFFFFF"
                fill-opacity="1.000000"
                fill-rule="nonzero"
              />
            </g>
          </svg>
        </button>
      </div>
      <form class="user-form">
        <div class="form-columns">
          <div
            v-for="(field, index) in userFields"
            :key="index"
            class="form-group"
          >
            <label :for="field.id">{{ field.label }}</label>
            <input
              :id="field.id"
              :placeholder="field.placeholder"
              :type="field.type"
            />
            <span v-if="index === 4" class="dropdown-icon"
              ><svg
                width="13.060669"
                height="7.591003"
                viewBox="0 0 13.0607 7.591"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
              >
                <desc>Created with Pixso.</desc>
                <defs />
                <path
                  id="Vector 4"
                  d="M0.53 0.53L6.53 6.53L12.53 0.53"
                  stroke="#718EBF"
                  stroke-opacity="1.000000"
                  stroke-width="1.500000"
                />
              </svg>
            </span>
          </div>
        </div>
        <button type="submit" class="save-button">Save</button>
      </form>
    </div>
  </div>
</template>
<script setup>
const userFields = [
  {
    id: 'Your Name',
    label: 'Your Name',
    placeholder: 'Charlene Reed ',
    type: 'text'
  },
  {
    id: 'User Name',
    label: 'User Name',
    placeholder: 'Charlene Reed ',
    type: 'text'
  },
  {
    id: 'Email',
    label: 'Email',
    placeholder: 'charlenereed@gmail.com ',
    type: 'email'
  },
  {
    id: 'Password',
    label: 'Password',
    placeholder: '**********',
    type: 'text'
  },
  {
    id: 'Date of Birth',
    label: 'Date of Birth',
    placeholder: '25 January 1990',
    type: 'text'
  },
  {
    id: 'Present Address',
    label: 'Present Address',
    placeholder: 'San Jose, California, USA',
    type: 'text'
  },
  {
    id: 'Permanent Address',
    label: 'Permanent Address',
    placeholder: 'San Jose, California, USA',
    type: 'text'
  },
  {
    id: 'City',
    label: 'City',
    placeholder: 'San Jose',
    type: 'text'
  },
  {
    id: 'Postal Code',
    label: 'Postal Code',
    placeholder: '45962',
    type: 'text'
  },
  {
    id: 'Country',
    label: 'Country',
    placeholder: 'USA',
    type: 'text'
  }
];
</script>
<style lang="scss" scoped>
.main-card {
  margin: 30px 40px 175px;
  border-radius: 25px;
  background: rgb(255, 255, 255);
  padding: 29px 31px;
}
.tabs {
  display: flex;
  gap: 45px;
  margin-bottom: 52px;
}
.tab {
  padding: 7px 15px 8px;
  border: none;
  background: none;
  cursor: pointer;
  font-size: 16px;
  color: rgb(113, 142, 191);
  font-family: Inter;
  font-size: 16px;
  font-weight: 500;
  line-height: 19px;
  letter-spacing: 0%;
  text-align: left;
}
.tab.active {
  color: rgb(24, 20, 243);
  padding: 9px 15px 8px;
  border-radius: 10px 10px 0px 0px;
  border-bottom: 3px solid rgb(24, 20, 243);
}
.user-info {
  display: flex;
  gap: 54px;
}
.avatar {
  position: relative;
  img {
    width: 130px;
    height: 130px;
    border-radius: 50%;
    padding-top: 4px;
  }
  .pencil {
    position: absolute;
    top: 87px;
    right: -1px;
    cursor: pointer;
    background: none;
    border: none;
    outline: none;
    width: 30px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgb(24, 20, 243);
    border-radius: 50%;
  }
}
.user-form {
  flex-grow: 1;
}
.form-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  row-gap: 23px;
  column-gap: 30px;
  padding-bottom: 31px;
}
.form-group {
  position: relative;
  display: flex;
  flex-direction: column;
  color: rgb(35, 35, 35);
  font-family: Inter;
  font-size: 16px;
  font-weight: 400;
  line-height: 19px;
  letter-spacing: 0;
  text-align: left;
  gap: 10px;
}
.form-group input {
  box-sizing: border-box;
  padding: 0 17px;
  height: 50px;
  border: 1px solid rgb(223, 234, 242);
  border-radius: 15px;
  background: rgb(255, 255, 255);
  color: rgb(113, 142, 191);
  font-family: Inter;
  font-size: 15px;
  font-weight: 400;
  line-height: 18px;
  letter-spacing: 0px;
  text-align: left;
}
.dropdown-icon {
  position: absolute;
  right: 23px;
  top: 68%;
  transform: translateY(-50%);
  pointer-events: none;
}
.save-button {
  width: 190px;
  height: 50px;
  color: rgb(255, 255, 255);
  font-family: Inter;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  letter-spacing: 0;
  text-align: center;
  border: none;
  cursor: pointer;
  align-self: flex-end;
  border-radius: 15px;
  background: rgb(24, 20, 243);
  float: right;
}
</style>
