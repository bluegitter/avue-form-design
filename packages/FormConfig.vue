<template>
  <div class="form-config-container">
    <el-form label-position="left"
             label-suffix="："
             label-width="130px">
      <el-form-item label="标签对齐方式"
                    placeholder="请选择按钮位置">
        <el-select v-model="data.labelPosition">
          <el-option label="左对齐"
                     value="left"></el-option>
          <el-option label="右对齐"
                     value="right"></el-option>
          <el-option label="顶部对齐"
                     value="top"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="表单字段宽度">
        <el-input-number v-model="data.labelWidth"
                         :min="80"
                         :max="200"
                         :step="10"
                         controls-position="right"
                         style="width: 100%"></el-input-number>
      </el-form-item>
      <el-form-item label="项之间的间隔">
        <el-input-number v-model="data.gutter"
                         :min="0"
                         :max="60"
                         :step="5"
                         controls-position="right"
                         style="width: 100%"></el-input-number>
      </el-form-item>
      <el-form-item label="显示按钮">
        <el-switch v-model="data.menuBtn"
                   active-color="#409EFF"></el-switch>
      </el-form-item>
      <el-form-item label="按钮位置"
                    v-if="data.menuBtn">
        <el-select v-model="data.menuPostion"
                   placeholder="请选择按钮位置">
          <el-option label="居左"
                     value="left"></el-option>
          <el-option label="居中"
                     value="center"></el-option>
          <el-option label="居右"
                     value="right"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="显示提交按钮"
                    v-if="data.menuBtn">
        <el-switch v-model="data.submitBtn"
                   active-color="#409EFF"></el-switch>
      </el-form-item>
      <el-form-item label="提交按钮的大小"
                    v-if="data.menuBtn && data.submitBtn">
        <el-select v-model="data.submitSize"
                   placeholder="请选择提交按钮的大小">
          <el-option label="正常"
                     value="medium"></el-option>
          <el-option label="小"
                     value="small"></el-option>
          <el-option label="超小"
                     value="mini"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="提交按钮的文字"
                    v-if="data.menuBtn && data.submitBtn">
        <el-input v-model="data.submitText"
                  placeholder="请输入提交按钮的文字"></el-input>
      </el-form-item>

      <el-form-item label="显示清空按钮"
                    v-if="data.menuBtn">
        <el-switch v-model="data.emptyBtn"
                   active-color="#409EFF"></el-switch>
      </el-form-item>
      <el-form-item label="清空按钮的大小"
                    v-if="data.menuBtn && data.emptyBtn">
        <el-select v-model="data.emptySize"
                   placeholder="请选择提交按钮的大小">
          <el-option label="正常"
                     value="medium"></el-option>
          <el-option label="小"
                     value="small"></el-option>
          <el-option label="超小"
                     value="mini"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item label="清空按钮的文字"
                    v-if="data.menuBtn && data.emptyBtn">
        <el-input v-model="data.emptyText"
                  placeholder="请输入提交按钮的文字"></el-input>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'form-config',
  props: ['data']
}
</script>
