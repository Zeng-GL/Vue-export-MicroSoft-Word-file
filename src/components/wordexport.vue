<template>
  <v-app id="inspire">
    <v-stepper v-model="e1">
      <v-stepper-header>
        <v-stepper-step :complete="e1 > 1" step="1">
          基本概要說明
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 2" step="2">
          家事商談服務簡介
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 3" step="3">
          家事商談服務辦理情形
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 4" step="4">
          家事商談服務績效
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 5" step="5">
          112年工作重點
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 6" step="6">
          督導及培訓機制
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 7" step="7">
          工作甘特圖
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step :complete="e1 > 8" step="8"> 經費概算 </v-stepper-step>
      </v-stepper-header>
      <v-stepper-items>
        <v-stepper-content step="1">
          <v-card class="mb-12">
            <v-container fluid>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-container fluid>
                    <!---->
                    <v-row justify="center">
                      <v-col cols="3" md="3" sm="3" bg="3">
                        <h3 class="mt-5">方案名稱</h3>
                      </v-col>
                      <v-col cols="9" md="9" sm="9" bg="9">
                        <v-text-field
                          label="請填寫方案名稱"
                          v-model="pName"
                        ></v-text-field>
                      </v-col>
                    </v-row>
                    <!---->
                    <v-row justify="center">
                      <v-col cols="3" md="3" sm="3" bg="3">
                        <h3 class="mt-5">背景說明</h3>
                      </v-col>
                      <v-col cols="9" md="9" sm="9" bg="9">
                        <v-textarea
                          outlined
                          label="請整體描述服務地區人口特性、離婚發展趨勢、問題需求等"
                          v-model="pStory"
                        ></v-textarea>
                      </v-col>
                    </v-row>
                    <!---->
                    <v-row justify="center">
                      <v-col cols="3" md="3" sm="3" bg="3">
                        <h3 class="mt-5">方案目標</h3>
                      </v-col>
                      <v-col cols="9" md="9" sm="9" bg="9">
                        <v-textarea
                          outlined
                          label="請說明提出本方案目的及預計達成目標"
                          v-model="pGoal"
                        ></v-textarea>
                      </v-col>
                    </v-row>
                    <!---->
                  </v-container>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">執行期間</h3>
                    </v-col>
                    <v-col cols="9" md="9" sm="9" bg="9">
                      <v-date-picker range v-model="pTime"></v-date-picker>
                    </v-col>
                  </v-row>
                  <!---->
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">組織簡介</h3>
                    </v-col>
                    <v-col cols="9" md="9" sm="9" bg="9">
                      <v-textarea
                        outlined
                        label="請摘要說明組織架構、人力配置、主要服務項目…等"
                        v-model="pIntro"
                      ></v-textarea>
                    </v-col>
                  </v-row>
                  <!---->
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn color="primary" @click="e1 = 2"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="2">
          <v-card class="mb-12">
            <v-container fluid>
              <v-row justify="center">
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">服務規劃理念及方向</h3>
                    </v-col>
                    <v-col cols="6" md="6" sm="6" bg="6">
                      <v-textarea outlined v-model="tIdea"></v-textarea>
                    </v-col>
                  </v-row>
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">服務方式</h3>
                    </v-col>
                    <v-col cols="6" md="6" sm="6" bg="6">
                      <v-textarea outlined v-model="tService"></v-textarea>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">服務流程</h3>
                    </v-col>
                    <v-col cols="6" md="6" sm="6" bg="6">
                      <v-textarea outlined v-model="tProcess"></v-textarea>
                    </v-col>
                  </v-row>
                  <v-row justify="center">
                    <v-col cols="3" md="3" sm="3" bg="3">
                      <h3 class="mt-5">服務內容</h3>
                    </v-col>
                    <v-col cols="6" md="6" sm="6" bg="6">
                      <v-textarea outlined v-model="tContent"></v-textarea>
                    </v-col>
                  </v-row>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 1"> 上一步 </v-btn>

          <v-btn color="primary" @click="e1 = 3"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="3">
          <v-card class="mb-12">
            <v-container fluid>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>合作縣市</h3>
                  <v-data-table
                    :headers="county_headers"
                    :items="county_items"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="c_dialog" max-width="600">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增合作對象
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">{{ c_formTitle }}</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-select
                                      v-model="c_editedItem.county"
                                      :items="county_select"
                                      label="縣市別"
                                    ></v-select>
                                  </v-col>
                                  <v-col cols="12" sm="1" md="1"></v-col>
                                  <v-col cols="12" sm="2" md="2">
                                    <h3 class="mt-5">年度</h3>
                                  </v-col>
                                  <v-col cols="12" sm="3" md="3">
                                    <v-radio-group
                                      v-model="c_editedItem.year"
                                      row
                                    >
                                      <v-radio
                                        label="110年"
                                        value="110年"
                                      ></v-radio>
                                      <v-radio
                                        label="111年"
                                        value="111年"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="12" sm="12" md="12">
                                    <v-textarea
                                      outlined
                                      v-model="c_editedItem.content"
                                      label="請簡述合作內容"
                                    ></v-textarea>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="c_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn color="blue darken-1" text @click="c_save">
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog v-model="c_dialogDelete" max-width="500px">
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="c_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="c_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon small class="mr-2" @click="c_editItem(item)">
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="c_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>合作法院</h3>
                  <v-data-table
                    :headers="law_headers"
                    :items="law_items"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="l_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增合作法院
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">{{ l_formTitle }}</span>
                            </v-card-title>
                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-select
                                      v-model="l_editedItem.law"
                                      :items="law_select"
                                      label="法院別"
                                    ></v-select>
                                  </v-col>
                                  <v-col cols="12" sm="1" md="1"></v-col>
                                  <v-col cols="12" sm="2" md="2">
                                    <h3 class="mt-5">年度</h3>
                                  </v-col>
                                  <v-col cols="12" sm="3" md="3">
                                    <v-radio-group
                                      v-model="l_editedItem.year"
                                      row
                                    >
                                      <v-radio
                                        label="110年"
                                        value="110年"
                                      ></v-radio>
                                      <v-radio
                                        label="111年"
                                        value="111年"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="12" sm="12" md="12">
                                    <v-textarea
                                      outlined
                                      v-model="l_editedItem.content"
                                      label="請簡述合作內容"
                                    ></v-textarea>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="l_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn color="blue darken-1" text @click="l_save">
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog v-model="l_dialogDelete" max-width="500px">
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="l_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="l_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon small class="mr-2" @click="l_editItem(item)">
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="l_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>經費來源</h3>
                  <v-data-table
                    :headers="money_headers"
                    :items="money_items"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="m_dialog" max-width="1000">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增經費來源
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">{{ m_formTitle }}</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-select
                                      v-model="m_editedItem.unit"
                                      :items="money_select"
                                      label="單位別"
                                    ></v-select>
                                  </v-col>
                                  <v-col cols="12" sm="1" md="1"></v-col>
                                  <v-col cols="12" sm="2" md="2">
                                    <h3 class="mt-5">年度</h3>
                                  </v-col>
                                  <v-col cols="12" sm="3" md="3">
                                    <v-radio-group
                                      v-model="m_editedItem.year"
                                      row
                                    >
                                      <v-radio
                                        label="110年"
                                        value="110年"
                                      ></v-radio>
                                      <v-radio
                                        label="111年"
                                        value="111年"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="4" sm="4" md="4">
                                    <v-radio-group
                                      v-model="m_editedItem.genre"
                                      row
                                      @change="step3_money_other_explain"
                                    >
                                      <v-radio
                                        label="委託費"
                                        value="委託費"
                                      ></v-radio>
                                      <v-radio
                                        label="補助費"
                                        value="補助費"
                                      ></v-radio>
                                      <v-radio
                                        label="其他"
                                        value="其他"
                                      ></v-radio>
                                    </v-radio-group>
                                    <v-textarea
                                      v-show="m_editedItem.genre == '其他'"
                                      outlined
                                      v-model="m_editedItem.other"
                                      label="請簡述其他經費來源"
                                    ></v-textarea>
                                  </v-col>
                                  <v-col cols="4" sm="4" md="4">
                                    <v-text-field
                                      v-model="m_editedItem.title"
                                      label="經費項目"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="4" sm="4" md="4">
                                    <v-text-field
                                      v-model="m_editedItem.amount"
                                      label="金額"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="m_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn color="blue darken-1" text @click="m_save">
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog v-model="m_dialogDelete" max-width="500px">
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="m_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="m_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon small class="mr-2" @click="m_editItem(item)">
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="m_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>111年工作人員名冊</h3>
                  <v-data-table
                    :headers="current_header"
                    :items="current_worker"
                    sort-by="calories"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog
                          v-model="current_worker_dialog"
                          max-width="500px"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增工作人員
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增工作人員</span>
                            </v-card-title>
                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="姓名"
                                      v-model="current_worker_editedItem.name"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="職稱"
                                      v-model="current_worker_editedItem.post"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-radio-group
                                      v-model="
                                        current_worker_editedItem.identity
                                      "
                                      row
                                    >
                                      <v-radio
                                        label="專任"
                                        value="專任"
                                      ></v-radio>
                                      <v-radio
                                        label="非專任"
                                        value="非專任"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-combobox
                                      v-model="current_worker_editedItem.bg"
                                      :items="current_worker_select"
                                      label="專業背景(可複選)"
                                      multiple
                                      outlined
                                      dense
                                      @change="step3_combobox_worker_other"
                                    ></v-combobox>
                                    <v-text-field
                                      label="請說明該專業人員身分"
                                      v-model="current_worker_editedItem.other"
                                      v-show="
                                        current_worker_editedItem.bg.includes('其他')
                                      "
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="學歷"
                                      v-model="current_worker_editedItem.study"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="經歷"
                                      v-model="current_worker_editedItem.exp"
                                    ></v-text-field>
                                  </v-col>

                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="從事家事商談服務年資"
                                      v-model="current_worker_editedItem.year"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="current_worker_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="current_worker_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="current_worker_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="current_worker_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="current_worker_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.actions`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="current_worker_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="current_worker_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                    <template v-slot:no-data>
                    </template>
                  </v-data-table>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 2"> 上一步 </v-btn>

          <v-btn color="primary" @click="e1 = 4"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="4">
          <v-card class="mb-12">
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="6">
                  <h3>個案來源(單位: 戶)</h3>
                  <v-data-table
                    :headers="test_headers"
                    :items="desserts"
                    item-key="name"
                    class="elevation-1"
                    :hide-default-footer="hideFooter"
                  >
                    <template v-slot:[`item.calories`]="props">
                      <v-edit-dialog
                        :return-value.sync="props.item.calories"
                        large
                        persistent
                        @save="save"
                        @cancel="cancel"
                        @open="open"
                        @close="close"
                      >
                        <div>{{ props.item.calories }}</div>
                        <template v-slot:input>
                          <div class="mt-4 text-h6">Update Iron</div>
                          <v-text-field
                            v-model="props.item.calories"
                            label="Edit"
                            single-line
                            counter
                            autofocus
                          ></v-text-field>
                        </template>
                      </v-edit-dialog>
                    </template>
                    <template v-slot:[`item.fat`]="props">
                      <v-edit-dialog
                        :return-value.sync="props.item.fat"
                        large
                        persistent
                        @save="save"
                        @cancel="cancel"
                        @open="open"
                        @close="close"
                      >
                        <div>{{ props.item.fat }}</div>
                        <template v-slot:input>
                          <div class="mt-4 text-h6">Update Iron</div>
                          <v-text-field
                            v-model="props.item.fat"
                            label="Edit"
                            single-line
                            counter
                            autofocus
                          ></v-text-field>
                        </template>
                      </v-edit-dialog>
                    </template>
                    <template v-slot:[`item.carbs`]="props">
                      <v-edit-dialog
                        :return-value.sync="props.item.carbs"
                        large
                        persistent
                        @save="save"
                        @cancel="cancel"
                        @open="open"
                        @close="close"
                      >
                        <div>{{ props.item.carbs }}</div>
                        <template v-slot:input>
                          <div class="mt-4 text-h6">Update Iron</div>
                          <v-text-field
                            v-model="props.item.carbs"
                            label="Edit"
                            single-line
                            counter
                            autofocus
                          ></v-text-field>
                        </template>
                      </v-edit-dialog>
                    </template>
                    <template v-slot:[`item.protein`]="props">
                      <v-edit-dialog
                        :return-value.sync="props.item.protein"
                        large
                        persistent
                        @save="save"
                        @cancel="cancel"
                        @open="open"
                        @close="close"
                      >
                        <div>{{ props.item.protein }}</div>
                        <template v-slot:input>
                          <div class="mt-4 text-h6">Update Iron</div>
                          <v-text-field
                            v-model="props.item.protein"
                            label="Edit"
                            single-line
                            counter
                            autofocus
                          ></v-text-field>
                        </template>
                      </v-edit-dialog>
                    </template>
                    <template v-slot:[`item.iron`]="props">
                      <v-edit-dialog
                        :return-value.sync="props.item.iron"
                        large
                        persistent
                        @save="save"
                        @cancel="cancel"
                        @open="open"
                        @close="close"
                      >
                        <div>{{ props.item.iron }}</div>
                        <template v-slot:input>
                          <div class="mt-4 text-h6">Update Iron</div>
                          <v-text-field
                            v-model="props.item.iron"
                            label="Edit"
                            single-line
                            counter
                            autofocus
                          ></v-text-field>
                        </template>
                      </v-edit-dialog>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="12" sm="6" md="6">
                  <h3>服務成果(單位: 戶)</h3>
                  <table border="3" class="step4_right_table">
                    <thead>
                      <tr>
                        <td></td>
                        <td colspan="2">服務家庭數</td>
                        <td colspan="2">服務人次</td>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <td></td>
                        <td>110年</td>
                        <td>111年1-4月</td>
                        <td>110年</td>
                        <td>111年1-4月</td>
                      </tr>
                      <tr>
                        <td>商談</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_talk"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                      <tr>
                        <td>心理諮商</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_mental"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                      <tr>
                        <td>子女會面交往</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_child"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                      <tr>
                        <td>諮詢</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_consult"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                      <tr>
                        <td>親職教育</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_edu"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                      <tr>
                        <td>其他(請逐項羅列)</td>
                        <td
                          contenteditable="true"
                          v-for="item in 4"
                          :key="item.id"
                          ref="step4_other"
                        ></td>
                      </tr>
                      <tr>
                        <td>合計</td>
                        <td v-for="item in 4" :key="item.id">
                          <input
                            ref="step4_total"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                    </tbody>
                  </table>
                </v-col>
              </v-row>
              <v-row>
                <v-col cols="12" sm="12" md="12">
                  <h3>服務成效</h3>
                </v-col>
                <v-col cols="12" sm="6" md="6">
                  <h4>成效評量方式</h4>
                  <v-textarea
                    outlined
                    v-model="sEva"
                    label="簡述，請說明施測對象、評量方式"
                  ></v-textarea>
                </v-col>
                <v-col cols="12" sm="6" md="6">
                  <h4>服務滿意度</h4>
                  <v-textarea
                    outlined
                    v-model="sHappy"
                    label="請說明施測數、回收數與相關統計分析"
                  ></v-textarea>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 3"> 上一步 </v-btn>
          <v-btn color="primary" @click="step4_submit_data"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="5">
          <v-card class="mb-12">
            <v-container fluid>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>合作縣市</h3>
                  <v-data-table
                    :headers="f_county_headers"
                    :items="c_future"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="f_county_dialog" max-width="600">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增合作對象
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增資料</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-select
                                      v-model="f_county_editedItem.county"
                                      :items="f_county_select"
                                      label="縣市別"
                                    ></v-select>
                                  </v-col>
                                  <v-col cols="12" sm="12" md="12">
                                    <v-textarea
                                      outlined
                                      v-model="f_county_editedItem.content"
                                      label="請簡述合作內容"
                                    ></v-textarea>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_county_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_county_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="f_county_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_county_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_county_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="f_county_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="f_county_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>合作法院</h3>
                  <v-data-table
                    :headers="f_law_headers"
                    :items="l_future"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="f_law_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增合作法院
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增合作法院</span>
                            </v-card-title>
                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-select
                                      v-model="f_law_editedItem.law"
                                      :items="f_law_select"
                                      label="法院別"
                                    ></v-select>
                                  </v-col>

                                  <v-col cols="12" sm="12" md="12">
                                    <v-textarea
                                      outlined
                                      v-model="f_law_editedItem.content"
                                      label="請簡述合作內容"
                                    ></v-textarea>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_law_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_law_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="f_law_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_law_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="f_law_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon small class="mr-2" @click="f_law_editItem(item)">
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="f_law_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
              </v-row>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>規劃工作人員</h3>
                  <v-data-table
                    :headers="s_worker_headers"
                    :items="s_worker_items"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="s_worker_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增工作人員
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增工作人員</span>
                            </v-card-title>
                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="姓名"
                                      v-model="s_worker_editedItem.name"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="職稱"
                                      v-model="s_worker_editedItem.post"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-radio-group
                                      v-model="s_worker_editedItem.identity"
                                      row
                                    >
                                      <v-radio
                                        label="專任"
                                        value="專任"
                                      ></v-radio>
                                      <v-radio
                                        label="非專任"
                                        value="非專任"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-combobox
                                      v-model="s_worker_editedItem.bg"
                                      :items="s_worker_select"
                                      label="專業背景(可複選)"
                                      multiple
                                      outlined
                                      dense
                                      @change="step5_combobox_worker_other"
                                    ></v-combobox>
                                    <v-text-field
                                      label="請說明該專業人員身分"
                                      v-model="s_worker_editedItem.other"
                                      v-show="s_worker_editedItem.bg == '其他'"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="學歷"
                                      v-model="s_worker_editedItem.study"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="經歷"
                                      v-model="s_worker_editedItem.exp"
                                    ></v-text-field>
                                  </v-col>

                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      label="從事家事商談服務年資"
                                      v-model="s_worker_editedItem.year"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="s_worker_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="s_worker_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="s_worker_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="s_worker_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="s_worker_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="s_worker_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="s_worker_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>規劃服務內容</h3>
                  <table border="3" class="step4_right_table">
                    <thead>
                      <tr>
                        <td rowspan="2">項目</td>
                        <td rowspan="2">辦理方式與內容(摘述)</td>
                        <td colspan="2">預計服務量</td>
                      </tr>
                      <tr>
                        <td>戶數/場次</td>
                        <td>人次</td>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="item in xxtest" :key="item.id">
                        <td>{{ item.title }}</td>
                        <td contenteditable="true" ref="step5_talk"></td>
                        <td>
                          <input
                            ref="step5_talk"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />戶
                        </td>
                        <td>
                          <input
                            ref="step5_talk"
                            type="number"
                            style="width: 100%"
                            @click="step4_clear_zero"
                          />
                        </td>
                      </tr>
                    </tbody>
                  </table>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 4"> 上一步 </v-btn>
          <v-btn color="primary" @click="step5_submit_data"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="6">
          <v-card class="mb-12">
            <v-container>
              <v-row>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3 class="mt-5">內部督導</h3>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <v-text-field
                    label="請填寫內部督導"
                    v-model="watch_inside"
                  ></v-text-field>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3 class="mt-5">外部督導</h3>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <v-text-field
                    label="請填寫外部督導"
                    v-model="watch_outside"
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row justify="center">
                <v-col cols="12" md="12" sm="12" bg="12">
                  <v-data-table
                    :headers="watch_headers"
                    :items="watch_items"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-dialog v-model="watch_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增督導人員
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增督導人員</span>
                            </v-card-title>
                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="6">
                                    <v-text-field
                                      v-model="watch_editedItem.name"
                                      label="請填寫督導人員姓名"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="1" md="1"></v-col>
                                  <v-col cols="12" sm="2" md="2">
                                    <h3 class="mt-5">身分</h3>
                                  </v-col>
                                  <v-col cols="12" sm="3" md="3">
                                    <v-radio-group
                                      v-model="watch_editedItem.identity"
                                      row
                                    >
                                      <v-radio
                                        label="內聘"
                                        value="內聘"
                                      ></v-radio>
                                      <v-radio
                                        label="外聘"
                                        value="外聘"
                                      ></v-radio>
                                    </v-radio-group>
                                  </v-col>
                                  <v-col cols="12" sm="12" md="12">
                                    <v-textarea
                                      outlined
                                      v-model="watch_editedItem.exp"
                                      label="經歷(相關專業背景)"
                                    ></v-textarea>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="watch_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="watch_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="watch_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="watch_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="watch_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.action`]="{ item }">
                      <v-icon small class="mr-2" @click="watch_editItem(item)">
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="watch_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                  </v-data-table>
                </v-col>
              </v-row>
              <v-row>
                <v-col cols="4" md="4" sm="4" bg="4">
                  <v-textarea
                    outlined
                    v-model="watch_worker"
                    label="工作人員培訓方式與內容(含職前訓練、在職訓練)"
                  ></v-textarea>
                </v-col>
                <v-col cols="4" md="4" sm="4" bg="4">
                  <v-textarea
                    outlined
                    v-model="watch_eva"
                    label="成效評量方式(列舉，應含質化與量化評量，並請說明施測對象、評量方式、工具)"
                  ></v-textarea>
                </v-col>
                <v-col cols="4" md="4" sm="4" bg="4">
                  <v-textarea
                    outlined
                    v-model="watch_expect"
                    label="預期效益(列舉，應含量化與質化分析)"
                  ></v-textarea>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 5"> 上一步 </v-btn>

          <v-btn color="primary" @click="e1 = 7"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="7">
          <v-card class="mb-12">
            <v-data-table
              :headers="gantt_headers"
              :items="gantt_items"
              class="elevation-1"
            >
              <template v-slot:[`item.jan`]="{ item }">
                <v-checkbox
                  v-model="item.check1"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.feb`]="{ item }">
                <v-checkbox
                  v-model="item.check2"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.mar`]="{ item }">
                <v-checkbox
                  v-model="item.check3"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.apr`]="{ item }">
                <v-checkbox
                  v-model="item.check4"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.may`]="{ item }">
                <v-checkbox
                  v-model="item.check5"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.jun`]="{ item }">
                <v-checkbox
                  v-model="item.check6"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.jly`]="{ item }">
                <v-checkbox
                  v-model="item.check7"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.aug`]="{ item }">
                <v-checkbox
                  v-model="item.check8"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.sep`]="{ item }">
                <v-checkbox
                  v-model="item.check9"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.oct`]="{ item }">
                <v-checkbox
                  v-model="item.check10"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.nov`]="{ item }">
                <v-checkbox
                  v-model="item.check11"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
              <template v-slot:[`item.dec`]="{ item }">
                <v-checkbox
                  v-model="item.check12"
                  false-value="X"
                  true-value="V"
                ></v-checkbox>
              </template>
            </v-data-table>
          </v-card>

          <v-btn text @click="e1 = 6"> 上一步 </v-btn>
          <v-btn color="primary" @click="step7_submit_data"> 下一步 </v-btn>
        </v-stepper-content>

        <v-stepper-content step="8">
          <v-card class="mb-12">
            <v-container fluid>
              <v-row>
                <v-col cols="12" md="12" sm="12" bg="12">
                  <h2>商談或心理諮商費</h2>
                </v-col>
              </v-row>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>1.個別</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_single[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_single[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_single[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_single[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_consult_single[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>2.共同/聯合</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_group[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_group[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_group[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_consult_group[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_consult_group[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
              </v-row>
              <!---->
              <v-row>
                <v-col cols="12" md="12" sm="12" bg="12">
                  <h2>子女會面交往服務輔導事務費</h2>
                </v-col>
              </v-row>
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>1.會面前評估會談及結案會談</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child1[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child1[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child1[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child1[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_child1[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <h3>2.會面交往執行</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child2[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child2[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child2[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_child2[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_child2[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
              </v-row>
              <!---->
              <v-row>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3>交通費</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_transport[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_transport[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_transport[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_transport[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_transport[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3>電話諮詢輔導事務費</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_phone[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_phone[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_phone[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_phone[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_phone[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3>個案諮詢鐘點費</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_clock[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_clock[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_clock[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_clock[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_clock[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
                <v-col cols="3" md="3" sm="3" bg="3">
                  <h3>甲類專案計畫管理費</h3>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_pm[0].price"
                    label="請填寫單價"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_pm[0].amount"
                    label="請填寫數量"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_pm[0].apply"
                    label="請填寫申請補助金額"
                  ></v-text-field>
                  <v-text-field
                    outlined
                    dense
                    v-model="fee_pm[0].self"
                    label="請填寫單位自籌金額"
                  ></v-text-field>
                  <v-textarea
                    outlined
                    v-model="fee_pm[0].note"
                    label="請簡述其他經費來源"
                  ></v-textarea>
                </v-col>
              </v-row>
              <!---->
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-data-table
                    :headers="fee_header_table"
                    :items="fee_activity"
                    sort-by="calories"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-toolbar-title>團體及活動費</v-toolbar-title>
                        <v-divider class="mx-4" inset vertical></v-divider>
                        <v-spacer></v-spacer>
                        <v-dialog
                          v-model="fee_activity_dialog"
                          max-width="500px"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增團體及活動支出項目
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增項目</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_activity_editedItem.name"
                                      label="補助項目"
                                    ></v-text-field>
                                    <v-text-field
                                      v-model="fee_activity_editedItem.price"
                                      label="單價"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_activity_editedItem.amount"
                                      label="數量"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_activity_editedItem.apply"
                                      label="申請補助"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_activity_editedItem.self"
                                      label="單位自籌"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_activity_editedItem.note"
                                      label="備註"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_activity_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_activity_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="fee_activity_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_activity_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_activity_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.actions`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="fee_activity_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="fee_activity_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                    <template v-slot:no-data> </template>
                  </v-data-table>
                </v-col>
                <!---->
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-data-table
                    :headers="fee_header_table"
                    :items="fee_promo"
                    sort-by="calories"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-toolbar-title>宣導推廣</v-toolbar-title>
                        <v-divider class="mx-4" inset vertical></v-divider>
                        <v-spacer></v-spacer>
                        <v-dialog v-model="fee_promo_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增宣導推廣支出項目
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增項目</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_promo_editedItem.name"
                                      label="補助項目"
                                    ></v-text-field>
                                    <v-text-field
                                      v-model="fee_promo_editedItem.price"
                                      label="單價"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_promo_editedItem.amount"
                                      label="數量"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_promo_editedItem.apply"
                                      label="申請補助"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_promo_editedItem.self"
                                      label="單位自籌"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_promo_editedItem.note"
                                      label="備註"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_promo_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_promo_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="fee_promo_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_promo_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_promo_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.actions`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="fee_promo_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="fee_promo_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                    <template v-slot:no-data> </template>
                  </v-data-table>
                </v-col>
              </v-row>
              <!---->
              <v-row>
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-data-table
                    :headers="fee_header_table"
                    :items="fee_watch"
                    sort-by="calories"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-toolbar-title>督導與訓練</v-toolbar-title>
                        <v-divider class="mx-4" inset vertical></v-divider>
                        <v-spacer></v-spacer>
                        <v-dialog v-model="fee_watch_dialog" max-width="500px">
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增督導訓練支出
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增項目</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_watch_editedItem.name"
                                      label="補助項目"
                                    ></v-text-field>
                                    <v-text-field
                                      v-model="fee_watch_editedItem.price"
                                      label="單價"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_watch_editedItem.amount"
                                      label="數量"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_watch_editedItem.apply"
                                      label="申請補助"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_watch_editedItem.self"
                                      label="單位自籌"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_watch_editedItem.note"
                                      label="備註"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_watch_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_watch_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="fee_watch_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_watch_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_watch_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.actions`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="fee_watch_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="fee_watch_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                    <template v-slot:no-data> </template>
                  </v-data-table>
                </v-col>
                <!---->
                <v-col cols="6" md="6" sm="6" bg="6">
                  <v-data-table
                    :headers="fee_header_table"
                    :items="fee_special"
                    sort-by="calories"
                    class="elevation-1"
                  >
                    <template v-slot:top>
                      <v-toolbar flat>
                        <v-toolbar-title
                          >創新及特殊需求服務工作方案</v-toolbar-title
                        >
                        <v-divider class="mx-4" inset vertical></v-divider>
                        <v-spacer></v-spacer>
                        <v-dialog
                          v-model="fee_special_dialog"
                          max-width="500px"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn
                              color="primary"
                              dark
                              class="mb-2"
                              v-bind="attrs"
                              v-on="on"
                            >
                              新增特殊支出項目
                            </v-btn>
                          </template>
                          <v-card>
                            <v-card-title>
                              <span class="text-h5">新增項目</span>
                            </v-card-title>

                            <v-card-text>
                              <v-container>
                                <v-row>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_special_editedItem.name"
                                      label="補助項目"
                                    ></v-text-field>
                                    <v-text-field
                                      v-model="fee_special_editedItem.price"
                                      label="單價"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_special_editedItem.amount"
                                      label="數量"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_special_editedItem.apply"
                                      label="申請補助"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_special_editedItem.self"
                                      label="單位自籌"
                                    ></v-text-field>
                                  </v-col>
                                  <v-col cols="12" sm="6" md="4">
                                    <v-text-field
                                      v-model="fee_special_editedItem.note"
                                      label="備註"
                                    ></v-text-field>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-card-text>

                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_special_close"
                              >
                                Cancel
                              </v-btn>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_special_save"
                              >
                                Save
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                        <v-dialog
                          v-model="fee_special_dialogDelete"
                          max-width="500px"
                        >
                          <v-card>
                            <v-card-title class="text-h5"
                              >Are you sure you want to delete this
                              item?</v-card-title
                            >
                            <v-card-actions>
                              <v-spacer></v-spacer>
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_special_closeDelete"
                                >Cancel</v-btn
                              >
                              <v-btn
                                color="blue darken-1"
                                text
                                @click="fee_special_deleteItemConfirm"
                                >OK</v-btn
                              >
                              <v-spacer></v-spacer>
                            </v-card-actions>
                          </v-card>
                        </v-dialog>
                      </v-toolbar>
                    </template>
                    <template v-slot:[`item.actions`]="{ item }">
                      <v-icon
                        small
                        class="mr-2"
                        @click="fee_special_editItem(item)"
                      >
                        mdi-pencil
                      </v-icon>
                      <v-icon small @click="fee_special_deleteItem(item)">
                        mdi-delete
                      </v-icon>
                    </template>
                    <template v-slot:no-data> </template>
                  </v-data-table>
                </v-col>
              </v-row>
            </v-container>
          </v-card>

          <v-btn text @click="e1 = 7"> 上一步 </v-btn>
          <v-btn color="primary" @click="export_word"> 匯出word檔案 </v-btn>
        </v-stepper-content>
      </v-stepper-items>
    </v-stepper>
  </v-app>
</template>

<script>
import docxtemplater from "docxtemplater";
import JSZipUtils from "jszip-utils";
import { saveAs } from "file-saver";
import JSZip from "jszip";

export default {
  name: "word",
  props: {},
  data() {
    return {
      // stepper
      e1: 1,
      // official form part 1
      pName: "",
      pStory: "",
      pGoal: "",
      pTime: ["2022-03-10", "2022-09-20"],
      pIntro: "",
      // official form part 2
      tIdea: "",
      tService: "",
      tProcess: "",
      tContent: "",
      // official form part 3
      county_headers: [
        {
          text: "縣市別",
          align: "start",
          sortable: false,
          value: "county",
        },
        { text: "年度", value: "year" },
        { text: "合作內容", value: "content" },
        { text: "操作", value: "action" },
      ],
      county_items: [],
      county_select: ["台北市", "新北市", "台中市", "高雄市"],
      c_editedIndex: -1,
      c_editedItem: {
        county: "",
        year: "",
        content: "",
      },
      c_defaultItem: {
        county: "",
        year: "",
        content: "",
      },
      c_dialog: false,
      c_dialogDelete: false,
      law_headers: [
        {
          text: "法院別",
          align: "start",
          sortable: false,
          value: "law",
        },
        { text: "年度", value: "year" },
        { text: "合作內容", value: "content" },
        { text: "操作", value: "action" },
      ],
      law_items: [],
      law_select: [
        "台北市地方法院",
        "新北市地方法院",
        "台中市地方法院",
        "高雄市地方法院",
      ],
      l_editedIndex: -1,
      l_editedItem: {
        law: "",
        year: "",
        content: "",
      },
      l_defaultItem: {
        county: "",
        year: "",
        content: "",
      },
      l_dialog: false,
      l_dialogDelete: false,
      money_headers: [
        { text: "年度", value: "year" },
        {
          text: "單位別",
          align: "start",
          sortable: false,
          value: "unit",
        },
        { text: "性質", value: "genre" },
        { text: "經費項目", value: "title" },
        { text: "金額(元)", value: "amount" },
        { text: "操作", value: "action" },
      ],
      money_items: [],
      money_select: ["單位1", "單位2", "單位3", "單位4"],
      m_editedIndex: -1,
      m_editedItem: {
        unit: "",
        genre: "",
        year: "",
        content: "",
        other: "",
        title: "",
        amount: "",
      },
      m_defaultItem: {
        unit: "",
        genre: "",
        year: "",
        content: "",
        other: "",
        title: "",
        amount: "",
      },
      m_dialog: false,
      m_dialogDelete: false,
      current_header: [
        {
          text: "姓名",
          sortable: false,
          value: "name",
          align: "center",
        },
        { text: "職稱", value: "post", align: "center" },
        { text: "身分", value: "identity", align: "center" },
        { text: "專業背景", value: "bg", align: "center" },
        { text: "學歷", value: "study", align: "center" },
        { text: "經歷", value: "exp", align: "center" },
        { text: "從事家事商談服務年資", value: "year", align: "center" },
        { text: "操作", value: "actions", align: "center" },
      ],
      current_worker: [],
      current_worker_dialog: false,
      current_worker_editedIndex: -1,
      current_worker_editedItem: {
        name: "",
        post: "",
        identity: "",
        bg: "",
        study: "",
        exp: "",
        year: "",
        other: "",
      },
      current_worker_defaultItem: {
        name: "",
        post: "",
        identity: "",
        bg: "",
        study: "",
        exp: "",
        year: "",
        other: "",
      },
      current_worker_dialogDelete: false,
      current_worker_select: ["社會工作", "心理", "法院家事調解委員", "其他"],

      // official form part 4
      hideFooter: true,
      test_headers: [
        {
          text: "年份",
          sortable: false,
          value: "name",
          align: "center",
        },
        { text: "地方政府轉介", value: "calories", align: "center" },
        { text: "法院轉介", value: "fat", align: "center" },
        { text: "民眾自行求助", value: "carbs", align: "center" },
        { text: "其他", value: "protein", align: "center" },
        { text: "合計", value: "iron", align: "center" },
      ],
      desserts: [
        {
          name: "110年",
          calories: 159,
          fat: 6,
          carbs: 24,
          protein: 4,
          iron: 1,
        },
        {
          name: "111年1-4月",
          calories: 237,
          fat: 9,
          carbs: 37,
          protein: 4,
          iron: 50,
        },
      ],
      sEffect_talk: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_mental: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_child: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_consult: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_edu: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_other: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEffect_total: [
        {
          t1: "",
          t2: "",
          t3: "",
          t4: "",
        },
      ],
      sEva: "",
      sHappy: "",
      // official form part 5 (112年工作重點)
      f_county_headers: [
        {
          text: "縣市別",
          align: "start",
          sortable: false,
          value: "county",
        },
        { text: "合作內容", value: "content" },
        { text: "操作", value: "action" },
      ],
      c_future: [],
      f_county_select: ["台北市", "新北市", "台中市", "高雄市"],
      f_county_editedIndex: -1,
      f_county_editedItem: {
        county: "",
        content: "",
      },
      f_county_defaultItem: {
        county: "",
        content: "",
      },
      f_county_dialog: false,
      f_county_dialogDelete: false,
      f_law_headers: [
        {
          text: "法院別",
          align: "start",
          sortable: false,
          value: "law",
        },
        { text: "合作內容", value: "content" },
        { text: "操作", value: "action" },
      ],
      l_future: [],
      f_law_select: [
        "台北市地方法院",
        "新北市地方法院",
        "台中市地方法院",
        "高雄市地方法院",
      ],
      f_law_editedIndex: -1,
      f_law_editedItem: {
        law: "",
        content: "",
      },
      f_law_defaultItem: {
        law: "",
        content: "",
      },
      f_law_dialog: false,
      f_law_dialogDelete: false,
      s_worker_headers: [
        {
          text: "姓名",
          sortable: false,
          value: "name",
          align: "center",
        },
        { text: "職稱", value: "post", align: "center" },
        { text: "身分", value: "identity", align: "center" },
        { text: "專業背景", value: "bg", align: "center" },
        { text: "學歷", value: "study", align: "center" },
        { text: "經歷", value: "exp", align: "center" },
        { text: "從事家事商談服務年資", value: "year", align: "center" },
        { text: "操作", value: "action", align: "center" },
      ],
      s_worker_items: [],
      s_worker_dialog: false,
      s_worker_editedIndex: -1,
      s_worker_editedItem: {
        name: "",
        post: "",
        identity: "",
        bg: "",
        study: "",
        exp: "",
        year: "",
        other: "",
      },
      s_worker_defaultItem: {
        name: "",
        post: "",
        identity: "",
        bg: "",
        study: "",
        exp: "",
        year: "",
        other: "",
      },
      s_worker_dialogDelete: false,
      s_worker_select: ["社會工作", "心理", "法院家事調解委員", "其他"],
      xxtest: [
        {
          id: 1,
          title: "商談",
        },
        {
          id: 2,
          title: "心理諮商",
        },
        {
          id: 3,
          title: "子女會面交往",
        },
        {
          id: 4,
          title: "諮詢",
        },
        {
          id: 5,
          title: "親職教育",
        },
        {
          id: 6,
          title: "宣導推廣",
        },
        {
          id: 7,
          title: "其他",
        },
      ],
      xxContent: [["event", "count", "people"]],
      // official form part 6 (督導)
      watch_inside: "",
      watch_outside: "",
      watch_headers: [
        {
          text: "姓名",
          sortable: false,
          value: "name",
          align: "center",
        },
        { text: "身分", value: "identity", align: "center" },
        { text: "經歷", value: "exp", align: "center" },
        { text: "操作", value: "action", align: "center" },
      ],
      watch_items: [],
      watch_editedIndex: -1,
      watch_editedItem: {
        name: "",
        identity: "",
        exp: "",
      },
      watch_defaultItem: {
        name: "",
        identity: "",
        exp: "",
      },
      watch_dialog: false,
      watch_dialogDelete: false,
      watch_worker: "",
      watch_eva: "",
      watch_expect: "",
      // official form part 7 (甘特圖)
      gantt_headers: [
        {
          text: "",
          align: "start",
          sortable: false,
          value: "name",
        },
        { text: "一月", value: "jan" },
        { text: "二月", value: "feb" },
        { text: "三月", value: "mar" },
        { text: "四月", value: "apr" },
        { text: "五月", value: "may" },
        { text: "六月", value: "jun" },
        { text: "七月", value: "jly" },
        { text: "八月", value: "aug" },
        { text: "九月", value: "sep" },
        { text: "十月", value: "oct" },
        { text: "十一月", value: "nov" },
        { text: "十二月", value: "dec" },
      ],
      gantt_items: [
        {
          name: "商談與心理諮商",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "子女會面交往",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "諮詢",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "親職教育",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "團體活動",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "宣導推廣",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "個案研討",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "教育訓練",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "內部督導",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
        {
          name: "外部督導",
          check1: "",
          check2: "",
          check3: "",
          check4: "",
          check5: "",
          check6: "",
          check7: "",
          check8: "",
          check9: "",
          check10: "",
          check11: "",
          check12: "",
        },
      ],
      // official form part 8 (經費概算)
      fee_consult_single: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_consult_group: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_child1: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_child2: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_transport: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_phone: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_clock: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_pm: [
        {
          price: "",
          amount: "",
          total: "",
          apply: "",
          self: "",
          note: "",
        },
      ],
      fee_header_table: [
        {
          text: "補助項目",
          align: "start",
          sortable: false,
          value: "name",
        },
        { text: "單價", value: "price" },
        { text: "數量", value: "amount" },
        { text: "申請補助", value: "apply" },
        { text: "單位自籌", value: "self" },
        { text: "備註", value: "note" },
        { text: "操作", value: "actions" },
      ],
      fee_activity: [],
      fee_activity_editedIndex: -1,
      fee_activity_editedItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_activity_defaultItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_activity_dialog: false,
      fee_activity_dialogDelete: false,

      fee_promo: [],
      fee_promo_editedIndex: -1,
      fee_promo_editedItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_promo_defaultItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_promo_dialog: false,
      fee_promo_dialogDelete: false,

      fee_watch: [],
      fee_watch_editedIndex: -1,
      fee_watch_editedItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_watch_defaultItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_watch_dialog: false,
      fee_watch_dialogDelete: false,

      fee_special: [],
      fee_special_editedIndex: -1,
      fee_special_editedItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_special_defaultItem: {
        name: "",
        price: 0,
        amount: 0,
        total: 0,
        apply: 0,
        self: 0,
        note: "",
      },
      fee_special_dialog: false,
      fee_special_dialogDelete: false,
    };
  },
  methods: {
    export_word() {
      if(this.fee_consult_single[0].price != "" && this.fee_consult_single[0].amount != ""){
        this.fee_consult_single[0].total =
        Number(this.fee_consult_single[0].price) *
        Number(this.fee_consult_single[0].amount);
      }else{
        alert("請填寫個別商談或心理諮商費單價及數量")
      }
      
      if(this.fee_consult_group[0].price != "" && this.fee_consult_group[0].amount != "" ){
              this.fee_consult_group[0].total =
        Number(this.fee_consult_group[0].price) *
        Number(this.fee_consult_group[0].amount);
      }else{
        alert("請填寫共同商談或心理諮商費單價及數量")
      }

      if(this.fee_child1[0].price != "" && this.fee_child1[0].amount != ""){
        this.fee_child1[0].total =
        Number(this.fee_child1[0].price) * Number(this.fee_child1[0].amount);
      }else{
        alert("請填寫會面前評估會談及結案會談單價及數量")
      }

      if(this.fee_child2[0].price != "" && this.fee_child2[0].amount != ""){
        this.fee_child2[0].total =
        Number(this.fee_child2[0].price) * Number(this.fee_child2[0].amount);
      }else{
        alert("請填寫會面交往執行單價及數量")
      }
      
      if(this.fee_transport[0].price != "" && this.fee_transport[0].amount != ""){
        this.fee_transport[0].total =
        Number(this.fee_transport[0].price) * Number(this.fee_transport[0].amount);
      }else{
        alert("請填寫交通費單價及數量")
      }

      if(this.fee_phone[0].price != "" && this.fee_phone[0].amount != ""){
         this.fee_phone[0].total =
        Number(this.fee_phone[0].price) * Number(this.fee_phone[0].amount);
      }else{
        alert("請填寫電話諮詢輔導事務費單價及數量")
      }
      
      if(this.fee_clock[0].price != "" && this.fee_clock[0].amount != ""){
         this.fee_clock[0].total =
        Number(this.fee_clock[0].price) * Number(this.fee_clock[0].amount);
      }else{
        alert("請填寫個案諮詢鐘點費單價及數量")
      }
      
      if(this.fee_pm[0].price != "" && this.fee_pm[0].amount != ""){
         this.fee_pm[0].total =
        Number(this.fee_pm[0].price) * Number(this.fee_pm[0].amount);
      }else{
        alert("請填寫甲類專案計畫管理費單價及數量")
      }

      if(this.fee_activity[0].price != "" && this.fee_activity[0].amount != ""){
         this.fee_activity[0].total =
        Number(this.fee_activity[0].price) *
        Number(this.fee_activity[0].amount);
      }else{
        this.fee_activity[0].total = 0
      }
      
      if(this.fee_promo[0].price != "" && this.fee_promo[0].amount != ""){
         this.fee_promo[0].total =
        Number(this.fee_promo[0].price) * Number(this.fee_promo[0].amount);
      }else{
        this.fee_promo[0].total = 0
      }

      if(this.fee_watch[0].price != "" && this.fee_watch[0].amount != ""){
        this.fee_watch[0].total =
        Number(this.fee_watch[0].price) * Number(this.fee_watch[0].amount);
      }else{
        this.fee_watch[0].total = 0
      }
      
      if(this.fee_special[0].price != "" && this.fee_special[0].amount != ""){
        this.fee_special[0].total =
        Number(this.fee_special[0].price) * Number(this.fee_special[0].amount);
      }else{
        this.fee_special[0].total = 0
      }
    
      for (let i = 0; i < this.money_items.length; i++) {
        if (this.money_items[i].genre == "其他") {
          this.money_items[i].other =
            ":(請說明" + this.money_items[i].other + ")";
        }
      }
      let file = {
        pName: this.pName,
        pStory: this.pStory,
        pGoal: this.pGoal,
        pTime: this.pTime.join(" ~ "),
        pIntro: this.pIntro,
        tIdea: this.tIdea,
        tService: this.tService,
        tProcess: this.tProcess,
        tContent: this.tContent,
        county_items: this.county_items,
        law_items: this.law_items,
        money_items: this.money_items,
        current_worker: this.current_worker,
        desserts: this.desserts,
        sEffect_talk: this.sEffect_talk,
        sEffect_mental: this.sEffect_mental,
        sEffect_child: this.sEffect_child,
        sEffect_consult: this.sEffect_consult,
        sEffect_edu: this.sEffect_edu,
        sEffect_other: this.sEffect_other,
        sEffect_total: this.sEffect_total,
        sEva: this.sEva,
        sHappy: this.sHappy,
        c_future: this.c_future,
        l_future: this.l_future,
        s_worker_items: this.s_worker_items,
        xxContent: this.xxContent,
        ///
        watch_inside: this.watch_inside,
        watch_outside: this.watch_outside,
        watch_items: this.watch_items,
        watch_eva: this.watch_eva,
        watch_expect: this.watch_expect,
        gantt_items: this.gantt_items,
        ///
        fee_consult_single: this.fee_consult_single,
        fee_consult_group: this.fee_consult_group,
        fee_child1: this.fee_child1,
        fee_child2: this.fee_child2,
        fee_transport: this.fee_transport,
        fee_phone: this.fee_phone,
        fee_clock: this.fee_clock,
        fee_pm: this.fee_pm,
        fee_activity: this.fee_activity,
        fee_promo: this.fee_promo,
        fee_watch: this.fee_watch,
        fee_special: this.fee_special,
      };
      JSZipUtils.getBinaryContent(
        "real-example.docx",
        function (error, content) {
          if (error) throw error;

          let zip = new JSZip(content);
          let doc = new docxtemplater().loadZip(zip);

          doc.setData(file);

          try {
            doc.render();
          } catch (e) {
            console.log(e);
          }
          let out = doc.getZip().generate({
            type: "blob",
            mimeType:
              "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
          });

          saveAs(out, "物件評估資料.docx");
        }
      );
    },
    c_editItem(item) {
      this.c_editedIndex = this.county_items.indexOf(item);
      this.c_editedItem = Object.assign({}, item);
      this.c_dialog = true;
    },

    c_deleteItem(item) {
      this.c_editedIndex = this.county_items.indexOf(item);
      this.c_editedItem = Object.assign({}, item);
      this.c_dialogDelete = true;
    },

    c_deleteItemConfirm() {
      this.county_items.splice(this.c_editedIndex, 1);
      this.c_closeDelete();
    },

    c_close() {
      this.c_dialog = false;
      this.$nextTick(() => {
        this.c_editedItem = Object.assign({}, this.c_defaultItem);
        this.c_editedIndex = -1;
      });
    },

    c_closeDelete() {
      this.c_dialogDelete = false;
      this.$nextTick(() => {
        this.c_editedItem = Object.assign({}, this.c_defaultItem);
        this.c_editedIndex = -1;
      });
    },

    c_save() {
      if (this.c_editedIndex > -1) {
        Object.assign(this.county_items[this.c_editedIndex], this.c_editedItem);
      } else {
        this.county_items.push(this.c_editedItem);
      }
      this.c_close();
    },
    l_editItem(item) {
      this.l_editedIndex = this.law_items.indexOf(item);
      this.l_editedItem = Object.assign({}, item);
      this.l_dialog = true;
    },

    l_deleteItem(item) {
      this.l_editedIndex = this.law_items.indexOf(item);
      this.l_editedItem = Object.assign({}, item);
      this.l_dialogDelete = true;
    },

    l_deleteItemConfirm() {
      this.law_items.splice(this.l_editedIndex, 1);
      this.l_closeDelete();
    },
    l_closeDelete() {
      this.l_dialogDelete = false;
      this.$nextTick(() => {
        this.l_editedItem = Object.assign({}, this.l_defaultItem);
        this.l_editedIndex = -1;
      });
    },
    l_close() {
      this.l_dialog = false;
      this.$nextTick(() => {
        this.l_editedItem = Object.assign({}, this.l_defaultItem);
        this.l_editedIndex = -1;
      });
    },
    l_save() {
      if (this.l_editedIndex > -1) {
        Object.assign(this.law_items[this.l_editedIndex], this.l_editedItem);
      } else {
        this.law_items.push(this.l_editedItem);
      }
      this.l_close();
    },
    m_editItem(item) {
      this.m_editedIndex = this.money_items.indexOf(item);
      this.m_editedItem = Object.assign({}, item);
      this.m_dialog = true;
    },

    m_deleteItem(item) {
      this.m_editedIndex = this.money_items.indexOf(item);
      this.m_editedItem = Object.assign({}, item);
      this.m_dialogDelete = true;
    },

    m_deleteItemConfirm() {
      this.money_items.splice(this.m_editedIndex, 1);
      this.m_closeDelete();
    },
    m_closeDelete() {
      this.m_dialogDelete = false;
      this.$nextTick(() => {
        this.m_editedItem = Object.assign({}, this.m_defaultItem);
        this.m_editedIndex = -1;
      });
    },
    m_close() {
      this.m_dialog = false;
      this.$nextTick(() => {
        this.m_editedItem = Object.assign({}, this.m_defaultItem);
        this.m_editedIndex = -1;
      });
    },
    m_save() {
      if (this.m_editedIndex > -1) {
        Object.assign(this.money_items[this.m_editedIndex], this.m_editedItem);
      } else {
        this.money_items.push(this.m_editedItem);
        // console.log(this.county_items)
      }
      this.m_close();
    },
    step3_money_other_explain(){
    },
    step3_combobox_worker_other(){
    },
    current_worker_editItem(item) {
      this.current_worker_editedIndex = this.current_worker.indexOf(item);
      this.current_worker_editedItem = Object.assign({}, item);
      this.current_worker_dialog = true;
    },

    current_worker_deleteItem(item) {
      this.current_worker_editedIndex = this.current_worker.indexOf(item);
      this.current_worker_editedItem = Object.assign({}, item);
      this.current_worker_dialogDelete = true;
    },

    current_worker_deleteItemConfirm() {
      this.current_worker.splice(this.current_worker_editedIndex, 1);
      this.current_worker_closeDelete();
    },
    current_worker_closeDelete() {
      this.current_worker_dialogDelete = false;
      this.$nextTick(() => {
        this.current_worker_editedItem = Object.assign({}, this.current_worker_defaultItem);
        this.current_worker_editedIndex = -1;
      });
    },
    current_worker_close() {
      this.current_worker_dialog = false;
      this.$nextTick(() => {
        this.current_worker_editedItem = Object.assign({}, this.current_worker_defaultItem);
        this.current_worker_editedIndex = -1;
      });
    },
    current_worker_save() {
      if (this.current_worker_editedIndex > -1) {
        Object.assign(this.current_worker[this.current_worker_editedIndex], this.current_worker_editedItem);
      } else {
        this.current_worker.push(this.current_worker_editedItem);
      }
      this.current_worker_close();
    },
    f_county_editItem(item) {
      this.f_county_editedIndex = this.c_future.indexOf(item);
      this.f_county_editedItem = Object.assign({}, item);
      this.f_county_dialog = true;
    },

    f_county_deleteItem(item) {
      this.f_county_editedIndex = this.c_future.indexOf(item);
      this.f_county_editedItem = Object.assign({}, item);
      this.f_county_dialogDelete = true;
    },

    f_county_deleteItemConfirm() {
      this.c_future.splice(this.f_county_editedIndex, 1);
      this.f_county_closeDelete();
    },
    f_county_closeDelete() {
      this.f_county_dialogDelete = false;
      this.$nextTick(() => {
        this.f_county_editedItem = Object.assign({}, this.f_county_defaultItem);
        this.f_county_editedIndex = -1;
      });
    },
    f_county_close() {
      this.f_county_dialog = false;
      this.$nextTick(() => {
        this.f_county_editedItem = Object.assign({}, this.f_county_defaultItem);
        this.f_county_editedIndex = -1;
      });
    },
    f_county_save() {
      if (this.f_county_editedIndex > -1) {
        Object.assign(
          this.c_future[this.f_county_editedIndex],
          this.f_county_editedItem
        );
      } else {
        this.c_future.push(this.f_county_editedItem);
      }
      this.f_county_close();
    },
    f_law_editItem(item) {
      this.f_law_editedIndex = this.l_future.indexOf(item);
      this.f_law_editedItem = Object.assign({}, item);
      this.f_law_dialog = true;
    },

    f_law_deleteItem(item) {
      this.f_law_editedIndex = this.l_future.indexOf(item);
      this.f_law_editedItem = Object.assign({}, item);
      this.f_law_dialogDelete = true;
    },

    f_law_deleteItemConfirm() {
      this.l_future.splice(this.f_law_editedIndex, 1);
      this.f_law_closeDelete();
    },
    f_law_closeDelete() {
      this.f_law_dialogDelete = false;
      this.$nextTick(() => {
        this.f_law_editedItem = Object.assign({}, this.f_law_defaultItem);
        this.f_law_editedIndex = -1;
      });
    },
    f_law_close() {
      this.f_law_dialog = false;
      this.$nextTick(() => {
        this.f_law_editedItem = Object.assign({}, this.f_law_defaultItem);
        this.f_law_editedIndex = -1;
      });
    },
    f_law_save() {
      if (this.f_law_editedIndex > -1) {
        Object.assign(
          this.l_future[this.f_law_editedIndex],
          this.f_law_editedItem
        );
      } else {
        this.l_future.push(this.f_law_editedItem);
      }
      this.f_law_close();
    },
    step4_submit_data() {
      this.e1 = 5;

      let talk = this.$refs.step4_talk;
      for (let i = 0; i < talk.length; i++) {
        if (talk[i].value == "") {
          talk[i].value = 0;
        }

        this.sEffect_talk[0].t1 = talk[0].value;
        this.sEffect_talk[0].t2 = talk[1].value;
        this.sEffect_talk[0].t3 = talk[2].value;
        this.sEffect_talk[0].t4 = talk[3].value;
      }

      let mental = this.$refs.step4_mental;
      for (let i = 0; i < mental.length; i++) {
        if (mental[i].value == "") {
          mental[i].value = 0;
        }
        this.sEffect_mental[0].t1 = mental[0].value;
        this.sEffect_mental[0].t2 = mental[1].value;
        this.sEffect_mental[0].t3 = mental[2].value;
        this.sEffect_mental[0].t4 = mental[3].value;
      }

      let child = this.$refs.step4_child;
      for (let i = 0; i < child.length; i++) {
        if (child[i].value == "") {
          child[i].value = 0;
        }
        this.sEffect_child[0].t1 = child[0].value;
        this.sEffect_child[0].t2 = child[1].value;
        this.sEffect_child[0].t3 = child[2].value;
        this.sEffect_child[0].t4 = child[3].value;
      }

      let consult = this.$refs.step4_consult;
      for (let i = 0; i < consult.length; i++) {
        if (consult[i].value == "") {
          consult[i].value = 0;
        }
        this.sEffect_consult[0].t1 = consult[0].value;
        this.sEffect_consult[0].t2 = consult[1].value;
        this.sEffect_consult[0].t3 = consult[2].value;
        this.sEffect_consult[0].t4 = consult[3].value;
      }

      let edu = this.$refs.step4_edu;
      for (let i = 0; i < edu.length; i++) {
        if (edu[i].value == "") {
          edu[i].value = 0;
        }
        this.sEffect_edu[0].t1 = edu[0].value;
        this.sEffect_edu[0].t2 = edu[1].value;
        this.sEffect_edu[0].t3 = edu[2].value;
        this.sEffect_edu[0].t4 = edu[3].value;
      }

      let other = this.$refs.step4_other;
      for (let i = 0; i < other.length; i++) {
        if (other[i].textContent == "") {
          other[i].textContent = 0;
        }
        this.sEffect_other[0].t1 = other[0].textContent;
        this.sEffect_other[0].t2 = other[1].textContent;
        this.sEffect_other[0].t3 = other[2].textContent;
        this.sEffect_other[0].t4 = other[3].textContent;
      }

      let total = this.$refs.step4_total;
      for (let i = 0; i < total.length; i++) {
        if (total[i].value == "") {
          total[i].value = 0;
        }
        this.sEffect_total[0].t1 = total[0].value;
        this.sEffect_total[0].t2 = total[1].value;
        this.sEffect_total[0].t3 = total[2].value;
        this.sEffect_total[0].t4 = total[3].value;
      }
    },
    step4_clear_zero(e) {
      if (e.target.value == 0) {
        e.target.value = "";
      }
    },
    s_worker_editItem(item) {
      this.s_worker_editedIndex = this.s_worker_items.indexOf(item);
      this.s_worker_editedItem = Object.assign({}, item);
      this.s_worker_dialog = true;
    },

    s_worker_deleteItem(item) {
      this.s_worker_editedIndex = this.s_worker_items.indexOf(item);
      this.s_worker_editedItem = Object.assign({}, item);
      this.s_worker_dialogDelete = true;
    },

    s_worker_deleteItemConfirm() {
      this.s_worker_items.splice(this.s_worker_editedIndex, 1);
      this.s_worker_closeDelete();
    },
    s_worker_closeDelete() {
      this.s_worker_dialogDelete = false;
      this.$nextTick(() => {
        this.s_worker_editedItem = Object.assign({}, this.s_worker_defaultItem);
        this.s_worker_editedIndex = -1;
      });
    },
    s_worker_save() {
      if (this.s_worker_editedIndex > -1) {
        Object.assign(
          this.s_worker_items[this.s_worker_editedIndex],
          this.s_worker_editedItem
        );
      } else {
        this.s_worker_items.push(this.s_worker_editedItem);
      }
      this.s_worker_close();
    },
    s_worker_close() {
      this.s_worker_dialog = false;
      this.$nextTick(() => {
        this.s_worker_editedItem = Object.assign({}, this.s_worker_defaultItem);
        this.s_worker_editedIndex = -1;
      });
    },
    step5_combobox_worker_other(){
      if(s_worker_editedItem.bg.indexOf("其他")== -1){
        this.s_worker_editedItem.other = ""
      }
    },
    step5_submit_data() {
      this.e1 = 6;
      // 將輸入的值取出來
      let output = [];
      let long = this.$refs.step5_talk;
      for (let i = 0; i < long.length; i++) {
        if (long[i].tagName == "TD") {
            long[i] = long[i].textContent;
        } else if (long[i].tagName == "INPUT") {
            long[i] = long[i].value;
        }
      }

      // 把大陣列切分成多個小陣列
      for (let i = 0; i < long.length; i += 3) {
        const chunk = long.slice(i, i + 3);
        output.push(chunk);
      }

      // 將陣列轉成指定key值的物件
      let keys = this.xxContent.shift();
      for (let i = 0; i < output.length; i++) {
        let obj = {};
        for (let k = 0; k < keys.length; k++) {
          obj[keys[k]] = output[i][k];
        }
        this.xxContent.push(obj);

        // 設定title
        this.$nextTick(() => {
          this.xxContent[0].label = "商談";
          this.xxContent[1].label = "心理諮商";
          this.xxContent[2].label = "子女會面交往";
          this.xxContent[3].label = "諮詢";
          this.xxContent[4].label = "親職教育";
          this.xxContent[5].label = "宣導推廣";
          this.xxContent[6].label = "其他";
        });
      }
    },
    ///
    watch_editItem(item) {
      this.watch_editedIndex = this.watch_items.indexOf(item);
      this.watch_editedItem = Object.assign({}, item);
      this.watch_dialog = true;
    },

    watch_deleteItem(item) {
      this.watch_editedIndex = this.watch_items.indexOf(item);
      this.watch_editedItem = Object.assign({}, item);
      this.watch_dialogDelete = true;
    },

    watch_deleteItemConfirm() {
      this.watch_items.splice(this.watch_editedIndex, 1);
      this.watch_closeDelete();
    },
    watch_closeDelete() {
      this.watch_dialogDelete = false;
      this.$nextTick(() => {
        this.watch_editedItem = Object.assign({}, this.watch_defaultItem);
        this.watch_editedIndex = -1;
      });
    },
    ///
    watch_close() {
      this.watch_dialog = false;
      this.$nextTick(() => {
        this.watch_editedItem = Object.assign({}, this.watch_defaultItem);
        this.watch_editedIndex = -1;
      });
    },
    watch_save() {
      if (this.watch_editedIndex > -1) {
        Object.assign(
          this.watch_items[this.watch_editedIndex],
          this.watch_editedItem
        );
      } else {
        this.watch_items.push(this.watch_editedItem);
      }
      this.watch_close();
    },

    step7_submit_data() {
      this.e1 = 8;
    },
    fee_activity_editItem(item) {
      this.fee_activity_editedIndex = this.fee_activity.indexOf(item);
      this.fee_activity_editedItem = Object.assign({}, item);
      this.fee_activity_dialog = true;
    },

    fee_activity_deleteItem(item) {
      this.fee_activity_editedIndex = this.fee_activity.indexOf(item);
      this.fee_activity_editedItem = Object.assign({}, item);
      this.fee_activity_dialogDelete = true;
    },

    fee_activity_deleteItemConfirm() {
      this.fee_activity.splice(this.fee_activity_editedIndex, 1);
      this.fee_activity_closeDelete();
    },

    fee_activity_close() {
      this.fee_activity_dialog = false;
      this.$nextTick(() => {
        this.fee_activity_editedItem = Object.assign(
          {},
          this.fee_activity_defaultItem
        );
        this.fee_activity_editedIndex = -1;
      });
    },

    fee_activity_closeDelete() {
      this.fee_activity_dialogDelete = false;
      this.$nextTick(() => {
        this.fee_activity_editedItem = Object.assign(
          {},
          this.fee_activity_defaultItem
        );
        this.fee_activity_editedIndex = -1;
      });
    },

    fee_activity_save() {
      if (this.fee_activity_editedIndex > -1) {
        Object.assign(
          this.fee_activity[this.fee_activity_editedIndex],
          this.fee_activity_editedItem
        );
      } else {
        this.fee_activity.push(this.fee_activity_editedItem);
      }
      this.fee_activity_close();
    },
    fee_promo_editItem(item) {
      this.fee_promo_editedIndex = this.fee_promo.indexOf(item);
      this.fee_promo_editedItem = Object.assign({}, item);
      this.fee_promo_dialog = true;
    },

    fee_promo_deleteItem(item) {
      this.fee_promo_editedIndex = this.fee_promo.indexOf(item);
      this.fee_promo_editedItem = Object.assign({}, item);
      this.fee_promo_dialogDelete = true;
    },

    fee_promo_deleteItemConfirm() {
      this.fee_promo.splice(this.fee_promo_editedIndex, 1);
      this.fee_promo_closeDelete();
    },

    fee_promo_close() {
      this.fee_promo_dialog = false;
      this.$nextTick(() => {
        this.fee_promo_editedItem = Object.assign(
          {},
          this.fee_promo_defaultItem
        );
        this.fee_promo_editedIndex = -1;
      });
    },

    fee_promo_closeDelete() {
      this.fee_promo_dialogDelete = false;
      this.$nextTick(() => {
        this.fee_promo_editedItem = Object.assign(
          {},
          this.fee_promo_defaultItem
        );
        this.fee_promo_editedIndex = -1;
      });
    },

    fee_promo_save() {
      if (this.fee_promo_editedIndex > -1) {
        Object.assign(
          this.fee_promo[this.fee_promo_editedIndex],
          this.fee_promo_editedItem
        );
      } else {
        this.fee_promo.push(this.fee_promo_editedItem);
      }
      this.fee_promo_close();
    },
    fee_watch_editItem(item) {
      this.fee_watch_editedIndex = this.fee_watch.indexOf(item);
      this.fee_watch_editedItem = Object.assign({}, item);
      this.fee_watch_dialog = true;
    },

    fee_watch_deleteItem(item) {
      this.fee_watch_editedIndex = this.fee_watch.indexOf(item);
      this.fee_watch_editedItem = Object.assign({}, item);
      this.fee_watch_dialogDelete = true;
    },

    fee_watch_deleteItemConfirm() {
      this.fee_watch.splice(this.fee_watch_editedIndex, 1);
      this.fee_watch_closeDelete();
    },

    fee_watch_close() {
      this.fee_watch_dialog = false;
      this.$nextTick(() => {
        this.fee_watch_editedItem = Object.assign(
          {},
          this.fee_watch_defaultItem
        );
        this.fee_watch_editedIndex = -1;
      });
    },

    fee_watch_closeDelete() {
      this.fee_watch_dialogDelete = false;
      this.$nextTick(() => {
        this.fee_watch_editedItem = Object.assign(
          {},
          this.fee_watch_defaultItem
        );
        this.fee_watch_editedIndex = -1;
      });
    },

    fee_watch_save() {
      if (this.fee_watch_editedIndex > -1) {
        Object.assign(
          this.fee_watch[this.fee_watch_editedIndex],
          this.fee_watch_editedItem
        );
      } else {
        this.fee_watch.push(this.fee_watch_editedItem);
      }
      this.fee_watch_close();
    },
    fee_special_editItem(item) {
      this.fee_special_editedIndex = this.fee_special.indexOf(item);
      this.fee_special_editedItem = Object.assign({}, item);
      this.fee_special_dialog = true;
    },

    fee_special_deleteItem(item) {
      this.fee_special_editedIndex = this.fee_special.indexOf(item);
      this.fee_special_editedItem = Object.assign({}, item);
      this.fee_special_dialogDelete = true;
    },

    fee_special_deleteItemConfirm() {
      this.fee_special.splice(this.fee_special_editedIndex, 1);
      this.fee_special_closeDelete();
    },

    fee_special_close() {
      this.fee_special_dialog = false;
      this.$nextTick(() => {
        this.fee_special_editedItem = Object.assign(
          {},
          this.fee_special_defaultItem
        );
        this.fee_special_editedIndex = -1;
      });
    },

    fee_special_closeDelete() {
      this.fee_special_dialogDelete = false;
      this.$nextTick(() => {
        this.fee_special_editedItem = Object.assign(
          {},
          this.fee_special_defaultItem
        );
        this.fee_special_editedIndex = -1;
      });
    },
    fee_special_save() {
      if (this.fee_special_editedIndex > -1) {
        Object.assign(
          this.fee_special[this.fee_special_editedIndex],
          this.fee_special_editedItem
        );
      } else {
        this.fee_special.push(this.fee_special_editedItem);
      }
      this.fee_special_close();
    },
    open(){},
    close(){},
    save(){},
    cancel(){},
  },
  mounted() {},
  computed: {
    c_formTitle() {
      return this.c_editedIndex === -1 ? "New Item" : "Edit Item";
    },
    l_formTitle() {
      return this.l_editedIndex === -1 ? "New Item" : "Edit Item";
    },
    m_formTitle() {
      return this.m_editedIndex === -1 ? "New Item" : "Edit Item";
    },
  },
};
</script>


<style scoped lang="scss">
.useful_info_box {
  border: 1px solid grey;
  padding: 3rem;
  text-align: start;
}
.step4_right_table {
  width: 100%;
  border-collapse: collapse;
}
</style>