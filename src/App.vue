<template>
  <div class="container">
    <div class="row">
      <add-employee-button
        @add-employee-button="showForm = true"
        class="add-employee"
        :disabled="tooManyUsersAdded"
      />
      <div v-if="showForm" class="form_mask">
        <add-new-employee @add-employee="add" />
      </div>
    </div>
    <div class="row-auto user_table">
      <div class="col-md-auto">
        <table class="table" id="all_table">
          <thead id="thead">
            <tr>
              <th scope="col">
                <div class="d-flex align-items-center">
                  <a href="#">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="20"
                      height="20"
                      viewBox="0 0 20 20"
                      fill="none"
                    >
                      <path
                        d="M13.0948 5.69849C15.1373 7.74093 15.1373 11.0524 13.0948 13.0948C11.0524 15.1373 7.74095 15.1373 5.6985 13.0948C3.65606 11.0524 3.65606 7.74093 5.6985 5.69849C7.74095 3.65605 11.0524 3.65605 13.0948 5.69849"
                        stroke="#8591AE"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                      <path
                        d="M15.8333 15.8333L13.0917 13.0917"
                        stroke="#8591AE"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                    </svg>
                  </a>
                  Business Name
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  <a href="#">
                    <closed-sign />
                  </a>
                  Team
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.66119 0.187909C3.9264 -0.0625281 4.35931 -0.0625281 4.62452 0.187909L7.69547 3.08781C8.119 3.48775 7.81588 4.16675 7.2138 4.16675L1.0719 4.16675C0.469825 4.16675 0.166704 3.48775 0.590237 3.08781L3.66119 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.62452 4.14559C4.35931 4.39602 3.9264 4.39602 3.66119 4.14559L0.590238 1.24568C0.166705 0.845743 0.469825 0.166748 1.0719 0.166748L7.2138 0.166749C7.81588 0.166749 8.119 0.845743 7.69547 1.24569L4.62452 4.14559Z"
                            fill="#2A355A"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                  <div class="last_th_el">
                    <a href="#">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="21"
                        height="20"
                        viewBox="0 0 21 20"
                        fill="none"
                      >
                        <path
                          d="M6.95239 8.33334L10.2857 11.6667L13.6191 8.33334"
                          stroke="#8591AE"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  <a href="#">
                    <closed-sign />
                  </a>
                  Role
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                  <div class="last_th_el">
                    <a href="#">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="21"
                        height="20"
                        viewBox="0 0 21 20"
                        fill="none"
                      >
                        <path
                          d="M6.95239 8.33334L10.2857 11.6667L13.6191 8.33334"
                          stroke="#8591AE"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  <a href="#" class="pe-1">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="20"
                      height="20"
                      viewBox="0 0 20 20"
                      fill="none"
                    >
                      <path
                        d="M13.0948 5.69849C15.1373 7.74093 15.1373 11.0524 13.0948 13.0948C11.0524 15.1373 7.74095 15.1373 5.6985 13.0948C3.65606 11.0524 3.65606 7.74093 5.6985 5.69849C7.74095 3.65605 11.0524 3.65605 13.0948 5.69849"
                        stroke="#8591AE"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                      <path
                        d="M15.8333 15.8333L13.0917 13.0917"
                        stroke="#8591AE"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                    </svg>
                  </a>
                  Gmail
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  <a href="#">
                    <closed-sign />
                  </a>
                  Birthday
                  <div class="ps-1">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                  <div class="last_th_el">
                    <a href="#">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="21"
                        height="20"
                        viewBox="0 0 21 20"
                        fill="none"
                      >
                        <path
                          d="M6.95239 8.33334L10.2857 11.6667L13.6191 8.33334"
                          stroke="#8591AE"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  Telegram
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">
                  Last Login
                  <div class="ps-2">
                    <div class="up_link">
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M3.51833 0.187909C3.78354 -0.0625281 4.21646 -0.0625281 4.48166 0.187909L7.55262 3.08781C7.97615 3.48775 7.67303 4.16675 7.07095 4.16675L0.929049 4.16675C0.326972 4.16675 0.0238514 3.48775 0.447384 3.08781L3.51833 0.187909Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                    <div>
                      <a href="#">
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="8"
                          height="5"
                          viewBox="0 0 8 5"
                          fill="none"
                        >
                          <path
                            d="M4.48167 4.14559C4.21646 4.39602 3.78354 4.39602 3.51834 4.14559L0.447385 1.24568C0.0238523 0.845743 0.326973 0.166748 0.929049 0.166748L7.07095 0.166749C7.67303 0.166749 7.97615 0.845743 7.55262 1.24569L4.48167 4.14559Z"
                            fill="#C2C9DA"
                          />
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </th>
              <th scope="col">
                <div class="d-flex align-items-center">User permision</div>
              </th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="user in users"
              v-bind:key="user.name"
              class="text-center"
            >
              <td>
                <img src="./assets/img/avatar.png" alt="" class="pe-2" />{{
                  user.name
                }}
              </td>
              <td>{{ user.team }}</td>
              <td>{{ user.role }}</td>
              <td>{{ user.gmail }}</td>
              <td>{{ user.birthday }}</td>
              <td>{{ user.telegram }}</td>
              <td>{{ user.lastLogin }}</td>
              <td>
                <a @click="selectedUser = user" href="#">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                  >
                    <path
                      d="M11.6932 6.74667L9.25317 4.30667"
                      stroke="#8591AE"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M4.16721 14H1.99988V11.8327C1.99988 11.656 2.06988 11.486 2.19521 11.3613L11.0845 2.47135C11.3452 2.21068 11.7672 2.21068 12.0272 2.47135L13.5279 3.97202C13.7885 4.23268 13.7885 4.65468 13.5279 4.91468L4.63854 13.8047C4.51388 13.93 4.34388 14 4.16721 14V14Z"
                      stroke="#8591AE"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                  Edit
                </a>
                <a @click="handleDelete(user)" href="#">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    fill="none"
                  >
                    <path
                      d="M5.49784 7.49894C5.49784 7.2228 5.27398 6.99894 4.99784 6.99894C4.72169 6.99894 4.49784 7.2228 4.49784 7.49894H5.49784ZM15.502 7.49894C15.502 7.2228 15.2781 6.99894 15.002 6.99894C14.7259 6.99894 14.502 7.2228 14.502 7.49894H15.502ZM12.1673 8.33262C12.1673 8.05648 11.9434 7.83262 11.6673 7.83262C11.3911 7.83262 11.1673 8.05648 11.1673 8.33262H12.1673ZM11.1673 14.1684C11.1673 14.4445 11.3911 14.6684 11.6673 14.6684C11.9434 14.6684 12.1673 14.4445 12.1673 14.1684H11.1673ZM8.83256 8.33262C8.83256 8.05648 8.6087 7.83262 8.33256 7.83262C8.05642 7.83262 7.83256 8.05648 7.83256 8.33262H8.83256ZM7.83256 14.1684C7.83256 14.4445 8.05642 14.6684 8.33256 14.6684C8.6087 14.6684 8.83256 14.4445 8.83256 14.1684H7.83256ZM3.74731 4.4979C3.47117 4.4979 3.24731 4.72176 3.24731 4.9979C3.24731 5.27404 3.47117 5.4979 3.74731 5.4979V4.4979ZM16.2525 5.4979C16.5287 5.4979 16.7525 5.27404 16.7525 4.9979C16.7525 4.72176 16.5287 4.4979 16.2525 4.4979V5.4979ZM6.19086 4.83979C6.10353 5.10176 6.24511 5.38492 6.50708 5.47224C6.76905 5.55957 7.05221 5.41799 7.13954 5.15601L6.19086 4.83979ZM7.11872 3.63733L7.59306 3.79545L7.5931 3.79533L7.11872 3.63733ZM8.70104 2.49686L8.70092 2.99686H8.70104V2.49686ZM11.2988 2.49686V2.99686L11.2994 2.99686L11.2988 2.49686ZM12.8828 3.63733L13.3573 3.47974L13.3572 3.47933L12.8828 3.63733ZM12.8601 5.15549C12.9472 5.41756 13.2302 5.55945 13.4922 5.47242C13.7543 5.38538 13.8962 5.10238 13.8092 4.84031L12.8601 5.15549ZM4.49784 7.49894V15.8357H5.49784V7.49894H4.49784ZM4.49784 15.8357C4.49784 17.0327 5.4682 18.0031 6.6652 18.0031V17.0031C6.02048 17.0031 5.49784 16.4805 5.49784 15.8357H4.49784ZM6.6652 18.0031H13.3346V17.0031H6.6652V18.0031ZM13.3346 18.0031C14.5316 18.0031 15.502 17.0327 15.502 15.8357H14.502C14.502 16.4805 13.9794 17.0031 13.3346 17.0031V18.0031ZM15.502 15.8357V7.49894H14.502V15.8357H15.502ZM11.1673 8.33262V14.1684H12.1673V8.33262H11.1673ZM7.83256 8.33262V14.1684H8.83256V8.33262H7.83256ZM3.74731 5.4979H16.2525V4.4979H3.74731V5.4979ZM7.13954 5.15601L7.59306 3.79545L6.64438 3.47922L6.19086 4.83979L7.13954 5.15601ZM7.5931 3.79533C7.75194 3.31842 8.19825 2.99674 8.70092 2.99686L8.70116 1.99686C7.76788 1.99663 6.93926 2.59387 6.64434 3.47933L7.5931 3.79533ZM8.70104 2.99686H11.2988V1.99686H8.70104V2.99686ZM11.2994 2.99686C11.8025 2.99623 12.2494 3.31801 12.4084 3.79533L13.3572 3.47933C13.062 2.59312 12.2323 1.9957 11.2982 1.99686L11.2994 2.99686ZM12.4083 3.79492L12.8601 5.15549L13.8092 4.84031L13.3573 3.47974L12.4083 3.79492Z"
                      fill="#8591AE"
                    />
                  </svg>
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import AddNewEmployee from "./components/AddNewEmployee.vue";
import ClosedSign from "./components/ClosedSign.vue";
import AddEmployeeButton from "./components/AddEmployeeButton.vue";

export default {
  name: "App",

  components: {
    ClosedSign,
    AddNewEmployee,
    AddEmployeeButton,
  },

  data() {
    return {
      number: 1,
      selectedUser: null,
      showForm: false,
      name: "",
      team: "",
      role: "",
      gmail: "",
      birthday: "",
      telegram: "",
      lastLogin: "",
      userPermision: "",
      users: [
        {
          name: "Sarah Conor",
          team: "Crosty",
          role: "TeamLead",
          gmail: "sarahconnor@gmail.com",
          birthday: "25.04.1994",
          telegram: "@sarahconnor",
          lastLogin: "03.11.2021",
          userPermision: "",
        },
        {
          name: "Arnold Brown",
          team: "Gunters",
          role: "Seo Specialist",
          gmail: "arnoldbrown@gmail.com",
          birthday: "12.04.1989",
          telegram: "@arnoldbrown",
          lastLogin: "02.11.2021",
          userPermision: "",
        },
        {
          name: "Ernest Eberly",
          team: "Flamethrower",
          role: "Semantic Specialist",
          gmail: "ernesteberly@gmail.com",
          birthday: "17.06.1993",
          telegram: "@ErnestEberly",
          lastLogin: "03.11.2021",
          userPermision: "",
        },
      ],
    };
  },

  computed: {
    tooManyUsersAdded() {
      return this.users.length > 4;
    },
  },

  methods: {
    add(newUser) {
      this.users.push(newUser);

      this.cleanForm();
    },

    cleanForm() {
      this.name = "";
      this.team = "";
      this.role = "";
      this.gmail = "";
      this.birthday = "";
      this.telegram = "";
      this.lastLogin = "";
      this.userPermision = "";

      this.showForm = false;
    },

    handleDelete(userToRemove) {
      this.users = this.users.filter((u) => u !== userToRemove);
    },
  },
};
</script>
<style src="./assets/bootstrap.min.css"></style>
