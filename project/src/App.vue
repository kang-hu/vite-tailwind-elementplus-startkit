<script setup>
import zhTw from 'element-plus/lib/locale/lang/zh-tw'
import {ref} from 'vue'
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import {ElDivider, ElConfigProvider ,ElContainer, ElHeader, ElAside, ElMain, ElFooter, ElDatePicker} from 'element-plus'

let locale = zhTw

</script>

<template>
  <el-config-provider :locale="locale">
    <div class="common-layout">
      <el-container>
        <el-header>Header</el-header>
        <el-container>
          <el-aside width="200px">Aside</el-aside>
          <el-container>
            <el-main >
              <h1 class="text-3xl font-bold mb-4">
                Hello!
              </h1>
            </el-main>
            <el-footer>露天市集國際資訊股份有限公司版權所有Copyright © PChome eBay Co., Ltd.r</el-footer>
          </el-container>
        </el-container>
      </el-container>
    </div>
  </el-config-provider>
</template>

<style>
</style>
